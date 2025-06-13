# Documentação Técnica – Automação de Patches com AWS Systems Manager

## 📚 Contexto

A empresa sofreu uma falha de segurança por falta de atualização em instâncias EC2. Foi solicitado que a equipe de administração de sistemas implementasse uma solução automatizada para garantir que todas as instâncias EC2 se mantivessem atualizadas com patches de segurança.

## 👥 Desafios

- Evitar impactos de desempenho
- Respeitar janelas de manutenção
- Minimizar esforço operacional

## 🧠 Solução

Implementamos o AWS Systems Manager Patch Manager em conjunto com Maintenance Windows, organizando as instâncias via tags e configurando baselines de patches personalizadas.

## 🔧 Etapas Técnicas

1. Preparação das instâncias (IAM Role + SSM Agent)
2. Definição de tags `PatchGroup`
3. Criação de Patch Baseline com aprovação automática
4. Configuração de Maintenance Window e tarefas de patch
5. Monitoramento via AWS Systems Manager Compliance

## 🧩 Considerações Finais

A solução é escalável, fácil de manter e respeita a disponibilidade dos sistemas, ao mesmo tempo em que fortalece a segurança da infraestrutura.
