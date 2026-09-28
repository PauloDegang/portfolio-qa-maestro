#  Automação de Testes Mobile - Sauce Labs Demo

**Projeto prático de automação End-to-End (E2E) focado na garantia de qualidade (QA) de aplicativos Android.**

#  Objetivo
Demonstrar a aplicação de boas práticas de Quality Assurance através da automação de fluxos críticos de um aplicativo de e-commerce, incluindo modularização de scripts e validações de segurança. Este repositório reflete cenários reais de uso, conectando documentação de testes (Test Cases) à execução automatizada.

# 🛠 Tecnologias e Ferramentas Utilizadas
- **Maestro.dev:** Framework para automação de testes nativos mobile.
- **YAML:** Estruturação lógica e sequencial dos scripts.
- **Android Emulator:** Ambiente de execução dos testes.
- **Excel/Google Sheets:** Planejamento e documentação dos Casos de Teste.

##  Estrutura do Projeto
A automação foi dividida de forma modular para evitar repetição de código e facilitar a manutenção:

- `Login.yaml`: Módulo base de autenticação (reutilizável).
- `Checkout.yaml`: Fluxo E2E de sucesso, desde a escolha do produto até a finalização da compra.
- `Logout.yaml`: Validação do encerramento de sessão, utilizando chamadas de sub-fluxos (`runFlow`).
- `Login_erro.yaml`: Teste negativo validando o bloqueio e mensagens de erro ao inserir credenciais inválidas.

##  Como Executar
1. Instale o [Maestro CLI](https://maestro.mobile.dev/).
2. Inicie o seu emulador Android com o aplicativo [MyDemoApp] (https://github.com/saucelabs/my-demo-app-android) instalado.
3. Clone este repositório.
4. No terminal, navegue até a pasta do projeto e execute o comando:
   ```bash
   maestro test Checkout.yaml
