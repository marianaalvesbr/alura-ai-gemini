# DeclaraAI - Seu assistente inteligente para a declaração do Imposto de Renda
![Captura de Tela do DeclaraAI](logo.png "DeclaraAI em Execução")
## ✨ Sobre o Projeto

O DeclaraAI é um assistente desenvolvido em Python, utilizando o poder da Inteligência Artificial Generativa (Google Gemini) e o Google Agent Development Kit (ADK), para auxiliar você no processo de declaração do Imposto de Renda no Brasil.

Com o DeclaraAI, você pode obter informações atualizadas sobre as regras e prazos do IR para um determinado ano e, o mais importante, analisar automaticamente o texto de seus documentos financeiros (como informes de rendimento e notas fiscais) para identificar e listar dados cruciais que precisam ser declarados.

Simplifique a organização dos seus documentos e tenha um ponto de partida inteligente para preencher sua declaração com mais confiança!

## 🚀 Funcionalidades

*   **Busca de Informações Gerais:** Obtém as regras, prazos e novidades sobre a declaração do Imposto de Renda para um ano específico, utilizando um agente de busca online.
*   **Análise de Informes de Rendimento:** Processa arquivos PDF de informes de rendimento para extrair fontes pagadoras, tipos de rendimento, valores (brutos, impostos retidos) e outras informações relevantes.
*   **Análise de Notas Fiscais:** Processa arquivos PDF de notas fiscais (médicas, educacionais, etc.) para extrair dados do prestador, valores pagos, descrição do serviço e identificar se são potencialmente dedutíveis, indicando onde declarar.
*   **Formatação Clara:** Apresenta as informações de forma organizada e fácil de ler no notebook.

## 🛠️ Tecnologias Utilizadas

*   Python
*   Jupyter Notebook (para execução interativa)
*   Google Generative AI SDK (`google-genai`)
*   Google Agent Development Kit (`google-adk`)
*   `PyPDF2` para leitura de PDFs
*   Bibliotecas auxiliares como `textwrap`, `requests`, `IPython.display`, `google.colab.files`

## Pré-requisitos

Para rodar este projeto, você precisa ter:

1.  Uma conta Google.
2.  Acesso à API do Google Gemini e uma chave de API (`GOOGLE_API_KEY`). Você pode obter uma em [Google AI Studio](https://aistudio.google.com/).
3.  Um ambiente de execução Python que suporte Jupyter Notebooks e, idealmente, o Google Colab para usar a funcionalidade de upload de arquivos (`google.colab.files`).

## ⚙️ Instalação e Uso (Google Colab)

A maneira mais fácil de rodar este projeto é no Google Colab:

1.  Abra o notebook `seu_notebook.ipynb` (substitua pelo nome real do seu arquivo) no Google Colab.
2.  **Configure sua Chave de API:**
    *   Clique no ícone de chave 🔑 (Secrets) no painel da esquerda.
    *   Clique em `+ New secret`.
    *   No campo **Name**, digite `GOOGLE_API_KEY`.
    *   No campo **Value**, cole sua chave de API do Google Gemini.
    *   Certifique-se de que a opção "Notebook access" para este secret está ativa (marcada).
3.  **Execute as Células Sequencialmente:**
    *   Vá executando cada célula do notebook uma por uma, na ordem em que aparecem.
    *   As primeiras células instalarão as bibliotecas necessárias e configurarão o acesso à API.
    *   Quando a célula que pede o **ano de consulta** for executada, digite o ano e pressione Enter.
    *   Quando a célula que pede o **upload dos informes de rendimento** for executada, um botão "Escolher arquivos" aparecerá na saída. Clique nele e selecione seus arquivos PDF de informes de rendimento.
    *   Quando a célula que pede o **upload das notas fiscais** for executada, outro botão "Escolher arquivos" aparecerá. Clique nele e selecione seus arquivos PDF de notas fiscais.
    *   Os agentes processarão as informações e exibirão os resumos na saída do notebook.

## 📝 Notas Importantes

*   O sucesso na extração de texto de PDFs depende da qualidade e do formato do arquivo. PDFs baseados em imagem (digitalizados sem OCR) não terão o texto extraído por `PyPDF2`.
*   A acurácia da análise e das sugestões dos agentes depende da clareza e do conteúdo dos documentos e das capacidades dos modelos Gemini utilizados (`gemini-2.0-flash`, `gemini-2.5-flash-preview-04-17` ou outros que você escolher).
*   Este projeto é um assistente e **não substitui a consulta a um profissional de contabilidade ou as informações oficiais da Receita Federal**. Use as informações geradas como um auxílio na organização e no preenchimento da sua declaração.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir "issues" para relatar bugs ou sugerir melhorias, ou enviar "pull requests" com código.

## Licença

---

**Disclaimer:** Este projeto utiliza modelos de IA que podem gerar informações imprecisas. Sempre verifique os dados e consulte fontes oficiais ou profissionais qualificados para a sua declaração do Imposto de Renda.
