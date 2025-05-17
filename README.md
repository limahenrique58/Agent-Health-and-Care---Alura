# Agente de Saúde Mental e Bem-Estar - Sistema Multi-Agente 

Este código Python implementa um sistema de agentes conversacionais para auxiliar
pessoas com problemas emocionais e promover exercícios, seguindo um padrão
inspirado no Agent Development Kit (ADK) do Google. Ele separa as responsabilidades
em múltiplos Agentes especializados, incluindo um novo Agente Mentor, Ferramentas
(Tools) e um Orquestrador.

## Configuração no Google Colab

Para executar este código no Google Colab, siga os passos abaixo:

1.  **Instalar a biblioteca google-generativeai:**
    Execute a seguinte linha em uma célula do seu notebook Colab:
    ```bash
    !pip install google-generativeai
    ```

2.  **Obter sua Chave de API do Google AI Studio:**
    Se você ainda não tem uma chave de API, acesse o Google AI Studio
    (https://aistudio.google.com/) e crie uma nova chave de API.

3.  **Configurar a Chave de API no Colab (Recomendado: Secrets Manager):**
    A forma mais segura de configurar sua chave de API no Google Colab é usando o
    Secrets Manager:
    * No menu à esquerda do Colab, clique no ícone de chave (`🔑`).
    * Clique em `Gerenciar secrets`.
    * Clique em `+ Novo secret`.
    * No campo `Nome`, inscreva um nome para o seu secret (por exemplo, `GOOGLE_API_KEY`).
    * No campo `Valor`, cole o valor da sua chave de API real.
    * Certifique-se de que a opção `Notebook access` está ativada para este secret.
    * No código abaixo, descomente as linhas que carregam a chave usando `userdata.get()`
        e comente a linha `API_KEY = "YOUR_API_KEY"`.
    * Substitua `'YOUR_API_KEY_NAME_IN_SECRETS'` pelo nome que você deu ao seu secret
        no Secrets Manager.

    Alternativamente (NÃO RECOMENDADO para chaves sensíveis), você pode substituir
    a string placeholder `"YOUR_API_KEY"` diretamente no código pela sua chave real,
    mas **tenha cuidado para não compartilhar seu notebook com a chave exposta**.

4.  **Executar o Código:**
    Execute as células do código no seu notebook Colab. A função `main()` iniciará
    o sistema de agentes e você poderá interagir com ele através da linha de comando
    no output da célula.
