# chatbot-barbearia-typebot
Chabot para atendimentos rapidos e personalizados

# 💈 Assistente Virtual Inteligente & Sistema de Agendamentos (Typebot)

> Um fluxo conversacional em No-Code desenvolvido para automatizar a jornada de atendimento e agendamento de uma barbearia, integrado diretamente com o Google Sheets para controle de horários e prevenção de conflitos.

---

## 🚀 Sobre o Projeto
Este projeto foi construído para resolver um grande gargalo em estabelecimentos locais: a perda de tempo com agendamentos manuais e o atrito no primeiro contato com o cliente. O chatbot automatiza a captação de dados, apresenta serviços e valores de forma intuitiva, gerencia a agenda dos profissionais e valida se o horário escolhido está disponível em tempo real.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Typebot:** Construção da árvore de decisão, lógica conversacional e manipulação de variáveis.
* **Google Sheets API:** Banco de dados relacional para consulta de horários disponíveis, salvamento de leads e atualização de agendamentos.
* **Regex (Expressões Regulares):** Validação estrita de nomes completos e formatos de números de WhatsApp.
* **No-Code / UX Conversacional:** Foco em retenção e clareza na experiência do usuário.

---

## 🔄 Arquitetura do Fluxo (Jornada do Usuário)

O fluxo do chatbot foi estruturado nas seguintes etapas lógicas:

1. **Apresentação & Boas-vindas:** Saudação inicial humanizada preparando o cliente para o atendimento rápido.
2. **Identificação com Validação (Regex):** 
   * Captura do **Nome Completo** e verificação de espaços/caracteres válidos.
   * Captura e validação do **WhatsApp** (garantindo o padrão de 10 a 11 dígitos com DDD).
3. **Catálogo de Serviços:** Exibição interativa de 15 opções de serviços com seus respectivos valores (de cortes tradicionais a quimicas e barboterapia).
4. **Seleção de Profissional:** Escolha entre os barbeiros disponíveis (*André, Pedro ou Pierre*).
5. **Captura de Data e Consulta de Agenda (Google Sheets):**
   * O usuário escolhe o dia desejado (com validação para não permitir datas retroativas).
   * O bot consulta na planilha os horários com status `"Disponivel"` para aquele dia específico.
6. **Prevenção de Conflitos e Confirmação:** 
   * O bot faz uma verificação dupla na base de dados para garantir que o horário escolhido não foi ocupado por outro cliente no mesmo segundo.
   * Caso esteja livre, atualiza a planilha, registra o agendamento e envia uma mensagem de confirmação detalhada.

---

## 📂 Arquivos do Projeto
* [`/json/prototipo-pierre.json`](./json/prototipo-pierre.json): O código-fonte estruturado do fluxo exportado do Typebot, permitindo a importação e visualização completa da árvore de decisão.

---

## 👤 Autor
Desenvolvido por Wellington Regis.  
📫 Entre em contato via [Seu LinkedIn] ou [Seu E-mail].
