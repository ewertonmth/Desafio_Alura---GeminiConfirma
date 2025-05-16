# 🔎 GeminiConfirma – Analisador Inteligente de Fakenews e Desinformação

**GeminiConfirma** é um sistema modular e enxuto de verificação automatizada de conteúdo, projetado para rodar 100% no Google Colab utilizando **Google Gemini 2.0 Flash** e técnicas de verificação factual em tempo real com fallback inteligente.

---

## 🧠 Como Funciona

O fluxo de análise é feito por **4 agentes autônomos**, que operam em sequência:

1. **Resumo Inteligente (Agente 1)**  
   Comprime o conteúdo original mantendo os fatos centrais (modelo com temperatura 0.3).

2. **Verificação Factual (Agente 2)**  
   Realiza buscas no Google (via Custom Search) para checagem automática, com **fallback embutido** caso a API falhe.

3. **Análise Linguística (Agente 3)**  
   Detecta sinais de linguagem manipulativa, sensacionalismo ou viés emocional.

4. **Parecer Final (Agente 4)**  
   Emite uma conclusão objetiva sobre a confiabilidade do texto, com justificativa baseada nos módulos anteriores.

---

## ⚠️ Atenção

É **ESSENCIAL executar todas as células do código na ordem exata em que estão dispostas no notebook**.  
Isso garante o funcionamento correto dos módulos e evita erros de referência ou inicialização.

---

## ⚙️ Requisitos

-Python 3.x(Google Colab)
-Conta no Google Cloud com API Key e CSE ID
-Gemini API Key (Google AI Studio)

---

## 🚀 Instalação e Execução

1. No Google Colab, instale o Gemini SDK:
   ```python
   !pip install -q google-generativeai
   ```

2. Configure suas chaves:
   ```python
   genai.configure(api_key="SUA_API_GEMINI")
   GOOGLE_API_KEY = "SUA_API_GOOGLE"
   GOOGLE_CSE_ID = "SEU_CSE_ID"
   ```

3. Execute o notebook e forneça o texto para análise:
   ```python
   texto_teste = input("Digite o texto da notícia ou conteúdo para análise:\n")
   resultado = analisar_texto_completo(texto_teste)
   ```

---

## 📌 Principais Recursos

- ✅ Totalmente executável em Google Colab  
- 📡 Verificação factual dinâmica via Google Search  
- 🧠 Integração com LLM (Gemini 2.0 Flash) sem dependência de frameworks pesados  
- 💡 Modular, comentado e com fallback automático  

---

## 📤 Exemplo de Saída

```text
--- Resumo ---
[Resumo objetivo do conteúdo]

--- Verificação Factual ---
[Checagem com base em resultados do Google]

--- Análise de Linguagem ---
[Detecção de sensacionalismo, viés, manipulação]

--- Parecer Final ---
[Conclusão sobre a confiabilidade da notícia]
```

---

## 🛡️ Licença

MIT License. Livre para fins acadêmicos, educacionais e projetos open source.
