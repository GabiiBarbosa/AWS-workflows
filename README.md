# AWS Step Functions

## 📋 Sobre este Laboratório

Este repositório documenta o aprendizado prático com **AWS Step Functions**, serviço de orquestração de workflows serverless da AWS. O objetivo é consolidar conhecimentos sobre criação, implementação e gestão de workflows automatizados.

---

## 🎯 Objetivos do Laboratório

- [x] Compreender os conceitos fundamentais do AWS Step Functions
- [x] Implementar workflows Standard e Express
- [x] Praticar integração com serviços AWS (Lambda, SNS, SQS)
- [x] Aprender tratamento de erros e padrões de resiliência
- [x] Desenvolver habilidades em monitoramento e troubleshooting

---

## Arquitetura do Projeto

### Workflow Principal: Processamento de Pedidos

[Validar Pedido] → [Processar Pagamento] → [Verificar Estoque] → [Preparar Envio]


### Componentes do Sistema

| Componente | Função | Tecnologia |
|------------|--------|------------|
| **Orquestração** | Coordena o fluxo do processo | AWS Step Functions |
| **Validação** | Valida dados do pedido | AWS Lambda |
| **Pagamento** | Processa transações financeiras | AWS Lambda |
| **Estoque** | Verifica disponibilidade | AWS Lambda |
| **Envio** | Prepara para entrega | AWS Lambda |

---

## Configuração e Implementação

### Pré-requisitos
- ✅ Conta AWS
- ✅ AWS CLI configurado
- ✅ Conhecimento básico em Lambda
- ✅ Permissões IAM adequadas


## Resultados e Métricas

### Métricas de Performance
- Tempo médio de execução: 2-5 minutos
- Taxa de sucesso: 95%+

### Cenários Testados

| Cenário |	Resultado |	Aprendizado|
|---------|-----------|------------|
| Pedido válido | ✅ Sucesso |	Fluxo completo funcionando |
| Pagamento recusado | ⚠️ Processado | Tratamento de erro eficaz|
| Sem produtos |	❌ Rejeitado | Validação preventiva |
| Timeout Lambda |	🔄 Retentativa |	Resiliência do sistema |

## Erros Comuns Encontrados
- ARN malformado
- Problema: arn::aws::lambda:::function:name
- Solução: arn:aws:lambda:region:account:function:name
- Função Lambda não encontrada
- Causa: Função não criada ou nome incorreto

Solução: Verificar existência via CLI ou Console
