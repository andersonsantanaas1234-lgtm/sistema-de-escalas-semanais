# 📅 Sistema Automatizado de Escalas Semanais

Um sistema prático para automatizar a criação de escalas de trabalho com base na disponibilidade dos colaboradores. Os funcionários respondem a uma enquete simples informando os dias em que podem trabalhar, e o sistema consolida esses dados para gerar a escala final da semana.

## 🚀 Como Funciona?

1. **Coleta de Disponibilidade:** Os funcionários acessam um formulário/enquete e marcam os dias da semana em que estão disponíveis.
2. **Processamento de Dados:** O sistema cruza os dias informados pelos colaboradores com a quantidade de vagas necessárias por dia.
3. **Geração da Escala:** É gerada uma grade final balanceada, priorizando a distribuição justa de turnos.

---

## 🛠️ Tecnologias Recomendadas

Dependendo de como você quer construir o projeto, sugerimos duas abordagens:

*   **Abordagem No-Code / Low-Code (Rápida):** Google Forms / Microsoft Forms + Google Sheets + Script de automação (Apps Script).
*   **Abordagem Full-Stack (Personalizada):** Frontend em React/Vue para a enquete e Backend em Node.js/Python com banco de dados (PostgreSQL/MongoDB) para rodar o algoritmo de escala.

---

## 📋 Regras de Negócio e Algoritmo

Para que o gerador de escala funcione corretamente, as seguintes regras devem ser implementadas no código:

*   **Mínimo de Colaboradores:** Garantir o número mínimo de pessoas exigido por dia de trabalho.
*   **Limite de Carga Horária:** Evitar que o mesmo funcionário seja escalado mais vezes do que o permitido por lei ou contrato.
*   **Descanso Obrigatório:** Respeitar o intervalo mínimo de descanso entre turnos.
*   **Prioridade:** Caso um dia tenha excesso de voluntários, o sistema deve priorizar quem trabalhou menos na semana anterior.

---

## 💻 Estrutura do Arquivo de Dados (Exemplo JSON)

Se você estiver desenvolvendo via código, o formato dos dados recebidos da enquete deve seguir esta estrutura:

```json
[
  {
    "nome": "João Silva",
    "disponibilidade": ["Segunda", "Terça", "Sexta"]
  },
  {
    "nome": "Maria Souza",
    "disponibilidade": ["Quarta", "Quinta", "Sábado", "Domingo"]
  }
]
```

---


Desenvolvido para otimizar a gestão de equipes e economizar tempo na montagem de escalas. 🕒
