# 📅 Sistema de Automatização de Escalas Semanais (SAES)

**Trabalho Acadêmico — Engenharia de Software**  
**Instituição:** Faculdade de Tecnologia (FATEC)  
**Professor Orientador:** Prof. Arnaldo  
**Discente:** Anderson Santana  

---

## 📌 Visão Geral do Projeto
O SAES é uma solução de software concebida para otimizar o processo de gestão e alocação de recursos humanos. O sistema automatiza a criação de escalas de trabalho semanais a partir da coleta ativa da disponibilidade dos colaboradores por meio de uma interface de enquetes (inputs binários de disponibilidade por dia da semana), reduzindo o tempo de planejamento logístico e mitigando erros de sobrecarga de turnos.

---

## 📋 Engenharia de Requisitos

### Requisitos Funcionais (RF)
*   **RF-001 [Declaração de Disponibilidade]:** O sistema deve permitir que o funcionário selecione múltiplos dias da semana em que está disponível para trabalhar por meio de uma interface binária (Sim/Não).
*   **RF-002 [Consolidação de Dados]:** O sistema deve processar as respostas e cruzar os dados com a demanda mínima diária de vagas exigida pela organização.
*   **RF-003 [Algoritmo de Escala]:** O sistema deve gerar uma grade de escala balanceada respeitando as restrições contratuais e limites de carga horária.
*   **RF-004 [Visualização e Exportação]:** O sistema deve exibir a escala final homologada de forma clara para o gestor e para a equipe.

### Requisitos Não-Funcionais (RNF)
*   **RNF-001 [Usabilidade]:** A interface da enquete deve ser responsiva e de fácil interação (mobile-friendly), garantindo alta taxa de adesão dos colaboradores.
*   **RNF-002 [Consistência de Dados]:** O backend deve garantir a integridade das respostas mesmo sob acessos simultâneos (concorrência) no período de fechamento da enquete.

---

## 🏗️ Modelagem e Artefatos do Projeto

A fundamentação teórica, modelagem de processos e arquitetura de banco de dados deste ecossistema de projetos foram baseadas nas seguintes referências e repositórios acadêmicos integrados:

*   **🗂️ Modelagem de Processos e Diagramas UML:** Os diagramas de Caso de Uso, Fluxo de Dados e Entidade-Relacionamento do ecossistema de software seguem os padrões estabelecidos na [Pasta de Diagramas UML](https://github.com).
*   **🚀 Projeto Integrador de Base:** A documentação conceitual e a estrutura de escopo inicial foram desenvolvidas com apoio do repositório base [Projeto Integrador - Semestre 1](https://github.com).
*   **📱 Arquitetura de Software e Interface:** A lógica de consumo de APIs e persistência dos dados tomou como referência arquitetural o modelo escalável do repositório [UniMove](http://github.com).

### Estrutura de Entrada de Dados (Payload JSON de Exemplo)
Para o processamento de regras do algoritmo, o sistema consome estruturas padronizadas de dados como o exemplo abaixo:

```json
{
  "colaborador_id": "FT-2026-AS",
  "nome": "Anderson Santana",
  "disponibilidade_dias": {
    "segunda": true,
    "terca": true,
    "quarta": false,
    "quinta": false,
    "sexta": true,
    "sabado": false,
    "domingo": false
  }
}
```

---

## 🔧 Como Executar o Projeto Localmente

1. Clone este repositório para a sua máquina local:
   ```bash
   git clone https://github.com
   ```
2. Navegue até a pasta do projeto:
   ```bash
   cd NOME-DO-REPOSITORIO
   ```
3. Instale as dependências estruturais (conforme o ambiente escolhido):
   ```bash
   npm install
   ```
4. Inicie o ambiente de desenvolvimento local:
   ```bash
   npm start
   ```

---
*Projeto desenvolvido como critério de avaliação para a disciplina de Engenharia de Software na FATEC.* 🚀
