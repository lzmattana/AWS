# Loja Virtual de Café - Arquitetura AWS

Este repositório contém a arquitetura proposta para uma loja virtual de café utilizando serviços da AWS. A arquitetura foi projetada para ser segura, escalável e otimizada em termos de custos.

## Visão Geral da Arquitetura

![Diagrama de Arquitetura]([link-para-seu-diagrama.png](https://github.com/lzmattana/AWS/blob/main/AWS-Loja-Cafe.drawio))

## Componentes Principais

### Frontend
- **Amazon S3**: Hospeda os arquivos estáticos do site.
- **Amazon CloudFront**: CDN para distribuição global do conteúdo.
- **AWS WAF**: Proteção contra ataques web.

### Backend
- **Amazon API Gateway**: Gerenciamento de APIs RESTful.
- **AWS Lambda**: Execução do código do backend serverless.
- **Amazon EventBridge**: Orquestração de eventos entre serviços.

### Banco de Dados
- **Amazon DynamoDB**: Armazenamento de dados de produtos e pedidos.
- **Amazon ElastiCache**: Cache para melhorar a performance.

### Segurança
- **AWS IAM**: Gerenciamento de acessos e permissões.
- **Amazon Cognito**: Autenticação e autorização de usuários.
- **AWS KMS**: Gerenciamento de chaves de criptografia.

### Monitoramento e Logs
- **Amazon CloudWatch**: Monitoramento e logs.
- **AWS X-Ray**: Análise e depuração de aplicações distribuídas.

### Processamento de Pagamentos
- **AWS Step Functions**: Orquestração do fluxo de processamento de pedidos.
- **Amazon SQS**: Fila de mensagens para desacoplamento de componentes.

## Justificativas das Escolhas

1. **Serverless**: A escolha de serviços serverless (Lambda, API Gateway) reduz custos operacionais e facilita a escalabilidade.

2. **Alta Disponibilidade**: O uso de múltiplas Zonas de Disponibilidade e serviços gerenciados pela AWS garante alta disponibilidade.

3. **Segurança em Camadas**: WAF, IAM, Cognito e KMS fornecem múltiplas camadas de segurança.

4. **Otimização de Performance**: CloudFront e ElastiCache melhoram a velocidade de entrega do conteúdo.

5. **Escalabilidade**: Auto Scaling nativo dos serviços serverless permite lidar com picos de tráfego.

6. **Observabilidade**: CloudWatch e X-Ray fornecem insights profundos sobre o desempenho e problemas potenciais.

## Próximos Passos

1. Implementar a infraestrutura usando AWS CloudFormation ou Terraform.
2. Desenvolver o código do frontend e das funções Lambda.
3. Configurar pipelines de CI/CD para automação de deployments.
4. Realizar testes de carga e segurança.
5. Implementar monitoramento e alertas.
