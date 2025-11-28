# DIOAWS
DIO AWS DESAFIO
RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 28/11/2025
Empresa: Abstergo Industries
Responsável: Fabio

Introdução

Este relatório apresenta o processo de implementação de ferramentas na Abstergo Industries, realizado por Fabio. O objetivo central foi selecionar e implementar três serviços AWS focados diretamente em redução de custos, mantendo a performance e aumentando a eficiência operacional.

Descrição do Projeto

O projeto foi dividido em três etapas, cada uma relacionada a um serviço AWS com impacto direto na diminuição dos gastos mensais da empresa.

Etapa 1: Amazon S3 + S3 Intelligent-Tiering

Foco da ferramenta: Redução de custos com armazenamento.

Descrição do caso de uso:
A empresa utilizava armazenamento padrão (S3 Standard) para arquivos de baixa utilização, gerando custos elevados. A migração para S3 Intelligent-Tiering permite que os objetos mudem automaticamente entre camadas de custo mais baixo, pagando menos por dados raramente acessados sem perda de disponibilidade.
Isso reduz de 18% a 40% dos custos de armazenamento, dependendo do volume.

Etapa 2: Amazon EC2 com Auto Scaling + Instâncias Spot

Foco da ferramenta: Economia em computação e elasticidade.

Descrição do caso de uso:
A empresa mantinha servidores EC2 ligados 24h por dia, mesmo quando havia baixa demanda.
Implementamos:

Auto Scaling para desligar instâncias quando não há tráfego

Instâncias Spot para cargas não críticas, reduzindo até 70% do custo
Esse ajuste diminuiu significativamente o gasto mensal com computação, sem afetar usuários ou aplicações.

Etapa 3: AWS Lambda + EventBridge

Foco da ferramenta: Corte de custos substituindo servidores por computação serverless.

Descrição do caso de uso:
Diversos scripts de manutenção e tarefas periódicas rodavam em EC2, consumindo máquinas inteiras para tarefas simples.
Migramos esses processos para:

AWS Lambda (paga apenas quando roda)

EventBridge (agenda tarefas sem servidor)
Essa abordagem zerou o custo de máquinas dedicadas, reduzindo despesas com servidores usados apenas para rotinas agendadas.

Conclusão

A implementação das ferramentas na Abstergo Industries gerou uma redução significativa e imediata nos gastos, especialmente nas áreas de armazenamento e computação. A combinação de S3 Intelligent-Tiering, EC2 com Auto Scaling/Spot e Lambda permitiu:

Otimização do uso de recursos

Redução de até 50% nos custos gerais da infraestrutura

Maior eficiência operacional

Menor necessidade de manutenção manual

Recomenda-se continuar monitorando métricas pelo AWS Cost Explorer e avaliar novas migrações para serviços serverless, visando manter os custos sob controle e garantir escalabilidade.

Anexos

Planilha comparativa de custos antes/depois

Arquitetura da solução

Relatórios do AWS Cost Explorer

Documentação interna de implantação

Assinatura do Responsável pelo Projeto:

Fabio Tiroli
