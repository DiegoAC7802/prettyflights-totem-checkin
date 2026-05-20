# Diretrizes do GitFlow - Módulo Totem de Check-in (PrettyFlights)

## Histórico de Auditoria de Operações

### Inicialização e Configuração Inicial
- Criada a branch permanente `main` na inicialização do repositório.
- Criada a branch permanente `develop` a partir de `main` para integrar todas as novas funcionalidades de desenvolvimento estáveis.

### Desenvolvimento de Feature (Módulo de Check-in)
- Criada a branch de feature temporária `feature/tela-checkin` a partir de `develop`.
- Implementado o sistema básico de leitura de dados e interface do totem do PrettyFlights.

### Preparação da Versão Semântica 1.0.0
- Criada a branch temporária de publicação `release/1.0.0` originada da `develop`.
- Código congelado para testes finais. Preparação e metadados ajustados para o deploy estável.

### Correção Emergencial de Erros (Hotfix 1.0.1)
- Identificado travamento crítico de runtime do aplicativo no totem em produção.
- Criada a branch temporária de correção `hotfix/1.0.1` diretamente a partir da `main`.
- Resolvida a falha de travamento crítico na leitura de dados na tela inicial.