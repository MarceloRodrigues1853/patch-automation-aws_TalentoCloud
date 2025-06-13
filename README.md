# Automação de Patches com AWS Systems Manager

Este projeto apresenta uma estratégia para automatizar a aplicação de patches em instâncias EC2 utilizando o **AWS Systems Manager Patch Manager**, promovendo segurança, eficiência operacional e conformidade.

## 💡 Objetivo

Garantir que todas as instâncias EC2 estejam atualizadas com os patches mais recentes, reduzindo riscos de segurança, com impacto mínimo no desempenho e utilizando janelas de manutenção apropriadas.

## 🛠️ Ferramentas Utilizadas

- AWS Systems Manager
  - Patch Manager
  - Maintenance Windows
  - State Manager
- EC2
- IAM Roles
- Tags de recursos
- AWS CLI (opcional)

## 📌 Estratégia Resumida

1. **Preparação das instâncias EC2**
   - Instalar o SSM Agent
   - Atribuir IAM Role com política `AmazonSSMManagedInstanceCore`

2. **Organização por tags**
   - Ex: `PatchGroup = Producao` ou `PatchGroup = Dev`

3. **Criação de Patch Baselines**
   - Aprovação automática para patches de segurança após 7 dias

4. **Definição de Maintenance Windows**
   - Ex: domingo, 02h–04h (produção)

5. **Execução automática via RunPatchBaseline**
   - Integrado ao Maintenance Window

6. **Monitoramento e compliance**
   - Usando o AWS Systems Manager Compliance

## ✅ Benefícios

- Minimiza intervenção manual
- Reduz erros humanos
- Mantém sistemas seguros
- Respeita horários de menor impacto

## 📂 Arquivos

- `[documentacao.md](https://github.com/MarceloRodrigues1853/patch-automation-aws_TalentoCloud/blob/main/documento.md)`: Detalhamento da tarefa e contexto
- `[exemplo-tags-e-patch-group.json](https://github.com/MarceloRodrigues1853/patch-automation-aws_TalentoCloud/blob/main/exemplo-tags-e-patch-goup.json)`: Exemplo de tags para EC2

## 📎 Link útil

[AWS Patch Manager – Documentação oficial](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-patch.html)
