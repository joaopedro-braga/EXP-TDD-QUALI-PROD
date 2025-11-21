# Plano de Experimento – Scoping e Planejamento

# **1. Identificação Básica**

## **1.1 Título do Experimento**

**Avaliação do Impacto da Técnica Test-Driven Development (TDD) na Qualidade e Produtividade de Desenvolvedores de Software**

## **1.2 ID / Código**

EXP-TDD-QUALI-PROD-2025

## **1.3 Versão e Histórico**

| Versão | Data       | Descrição               |
| ------ | ---------- | ----------------------- |
| v1.0   | 20/11/2025 | Versão inicial do plano |

## **1.4 Datas**

* Data de criação: **20/11/2025**
* Última atualização: **20/11/2025**

## **1.5 Autores**

| Nome                   | Área                   | Contato                                                   |
| ---------------------- | ---------------------- | --------------------------------------------------------- |
| João Pedro Silva Braga | Engenharia de Software | [joao.psbraga6@gmail.com](mailto:joao.psbraga6@gmail.com) |

## **1.6 Responsável Principal (PI)**

João Pedro Silva Braga

## **1.7 Projeto / Iniciativa Relacionada**

Trabalho Final de Medição e Experimentação de Software – Engenharia de Software
Tema: Avaliando o Impacto da Técnica Test-Driven Development (TDD) na Qualidade e Produtividade de Desenvolvedores de Software

---

# **2. Contexto e Problema**

## **2.1 Descrição do Problema / Oportunidade**

Apesar de amplamente discutido na literatura, o real impacto do Test-Driven Development (TDD) na qualidade e produtividade ainda apresenta resultados divergentes. Alguns estudos apontam que TDD reduz defeitos e melhora o design do software, enquanto outros sugerem impacto negativo ou neutro na produtividade — especialmente em ambientes com desenvolvedores iniciantes.
No contexto educacional, essa lacuna é ainda maior, pois estudantes geralmente apresentam menor familiaridade com TDD, o que pode influenciar o desempenho. Assim, torna-se relevante investigar os efeitos da técnica em mini-projetos acadêmicos controlados.

## **2.2 Contexto Organizacional e Técnico**

* Ambiente: laboratório acadêmico controlado
* Participantes: estudantes de Engenharia de Software
* Tecnologias envolvidas: Java, JUnit 5, VSCode
* Processo: mini-projetos individuais com requisitos definidos e escopo limitado
* Ferramentas de apoio: Git, GitHub, planilhas de coleta de métricas, JUnit
* Treinamento: breve capacitação inicial em TDD para reduzir impacto da curva de aprendizado

## **2.3 Trabalhos e Evidências Prévias**

* **Beck (2003)** – *Test-Driven Development: By Example*: descreve fundamentos e sugere melhoria de design e redução de defeitos.
* **Nagappan, Maximilien, Bhat & Williams (2008)** – estudo industrial indicando aumento de qualidade, porém redução de produtividade em equipes da Microsoft.
* **Rafique & Mišić (2013)** – meta-análise (*IEEE TSE*) mostrou efeitos positivos, porém pequenos, na qualidade e impacto incerto na produtividade.
* Experimentos anteriores em sala indicam forte variabilidade no desempenho entre estudantes, reforçando necessidade de replicação.

## **2.4 Referencial Teórico e Empírico**

* TDD é uma prática ágil baseada no ciclo: **escrever o teste → implementar o código → refatorar**.
* Métricas de qualidade:

  * número de defeitos encontrados por revisão ou testes funcionais
  * cobertura de testes (line/branch)
  * severidade dos defeitos
* Métricas de produtividade:

  * tempo total para completar as tarefas
  * taxa de produção (LOC/hora), usada apenas como medida complementar
* Hipóteses clássicas fundamentadas na literatura:

  * **H1:** TDD melhora a qualidade do software.
  * **H2:** O impacto de TDD na produtividade é incerto e pode ser negativo em desenvolvedores iniciantes.
* Considerações metodológicas:

  * Defeitos serão contabilizados por meio de revisão estruturada e execução de testes independentes.
  * Cobertura de testes será utilizada como métrica complementar de qualidade, não como substituto da detecção de defeitos.
