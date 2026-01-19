# Complementos do Projeto AWS – Otimização de Custos

Este documento reúne **diagramas de arquitetura**, **estimativa de custos (antes/depois)** e **exemplos de scripts**, prontos para enriquecer o portfólio no GitHub.

---

## 📐 Diagrama de Arquitetura (Descrição)

**Fluxo proposto:**
- Usuários acessam a aplicação.
- Requisições são processadas por **AWS Lambda** (serverless).
- Dados e arquivos são armazenados no **Amazon S3 Intelligent-Tiering**.
- Serviços legados ou workloads variáveis rodam em **EC2 Auto Scaling**.
- Monitoramento de custos via **AWS Cost Explorer**.

**Benefícios:**
- Eliminação de servidores ociosos
- Pagamento por uso
- Escalabilidade automática

> Dica: gere o diagrama no Draw.io ou Lucidchart usando ícones oficiais da AWS e salve em `/diagramas/arquitetura.png`.

---

## 💰 Estimativa de Custos (Antes x Depois)

| Item | Antes (Infra Tradicional) | Depois (AWS Otimizada) |
|------|---------------------------|-------------------------|
| Servidores EC2 fixos | Alto (24/7) | Reduzido (Auto Scaling) |
| Armazenamento | S3 Standard | S3 Intelligent-Tiering |
| Processamento | Servidores dedicados | AWS Lambda |
| Custo mensal estimado | 100% | ~60% |

**Resultado esperado:** economia aproximada de **40%**.

> Dica: inclua uma planilha em `/planilhas/custos.xlsx` com cenários reais.

---

## 🧩 Exemplo de Script AWS Lambda (Python)

```python
import json

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': json.dumps('Processamento realizado com sucesso!')
    }
```

**Caso de uso:** processamento sob demanda de dados, logs ou eventos.

---

## 📦 Estrutura Final do Repositório

```
aws-cost-optimization-project/
│
├── README.md
├── RELATORIO_IMPLEMENTACAO_AWS.md
├── COMPLEMENTOS.md
├── diagramas/
│   └── arquitetura.png
├── planilhas/
│   └── custos.xlsx
└── scripts/
    └── lambda_exemplo.py
```

---

## 🚀 Próximos Passos (Opcional)
- Adicionar **Terraform ou CloudFormation**
- Criar **CI/CD com GitHub Actions**
- Publicar um **post no LinkedIn** explicando o case

Esse conjunto deixa seu projeto **nível pleno/sênior** para entrevistas técnicas 😎

