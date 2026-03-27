---
layout: post
title: "Migração Técnica: Do Looker Studio ao Streamlit"
date: 2026-03-27
categories: linguistica-computacional, morfologia
tags: [streamlit, python, regex, morfologia, gremd-usp, nlp]
---

Exploro aqui a transição do dashboard de busca do Dicionário Informal de uma solução "no-code" (Looker Studio) para uma arquitetura personalizada em Python com Streamlit.

### O Problema
O dashboard original cumpria o papel de visualização básica, mas apresentava limitações críticas para a análise linguística avançada: filtros engessados que dificultavam o uso de Regex e uma interatividade limitada para buscas morfológicas complexas.

### A Solução: Python + Streamlit
A migração permitiu um controle granular sobre o processamento dos dados. Implementei:

* **Busca por Símbolos (Regex):** Lógica automática onde o sistema identifica prefixos (`+*`), sufixos (`*+`) ou palavras isoladas (`.termo.`).
* **Normalização de Strings:** Tratamento de strings para ignorar acentos e variações de caixa, garantindo integridade na recuperação dos dados.
* **Exportação Otimizada:** Configuração de codificação `utf-8-sig` e separadores específicos (`;`) para garantir compatibilidade direta com o Excel.

### Resultado
A ferramenta agora é um artefato funcional que une rigor técnico e usabilidade, facilitando a coleta de dados para o GREMD-USP. Todo o projeto é versionado e documentado via GitHub.

---

**[/ acessar_dashboard ↗](https://buscador-di.streamlit.app/)** **[/ ver_repositorio ↗](https://github.com/glosa-lab/buscador-di)**
