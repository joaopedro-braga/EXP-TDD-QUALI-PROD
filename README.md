# Plano de Experimento – Scoping e Planejamento

# **1. Identificação Básica**

## **1.1 Título do Experimento**

**Avaliação do Impacto da Técnica Test-Driven Development (TDD) na Qualidade e Produtividade de Desenvolvedores de Software**

## **1.2 ID / Código**

EXP-TDD-QUALI-PROD-2025

## **1.3 Versão e Histórico**

| Versão | Data       | Descrição               |
| ------ | ---------- | ----------------------- |
| v1.0   | 20/11/2025 | Versão inicial do plano (Scoping e Contexto) |

## **1.4 Datas**

* Data de criação: **20/11/2025**
* Última atualização: **25/11/2025**

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
Apesar de amplamente discutido na literatura, o real impacto do *Test-Driven Development* (TDD) apresenta resultados divergentes. Enquanto defensores alegam melhoria na qualidade interna e externa do software, estudos empíricos apontam possíveis reduções na produtividade, especialmente em ambientes com desenvolvedores iniciantes (curva de aprendizado).
No contexto educacional e de formação de novos engenheiros, essa lacuna é crítica: sem evidências claras, é difícil justificar o *trade-off* do esforço inicial do TDD. Assim, torna-se relevante investigar os efeitos da técnica em **problemas de tamanho controlado ("toy problems")** para isolar variáveis de confusão.

## **2.2 Contexto Organizacional e Técnico**
O experimento será conduzido seguindo a classificação de contexto de experimentação (Basili et al./Wohlin):
*   **Ambiente:** *Off-line* (laboratório acadêmico controlado, sem pressão de produção industrial).
*   **Participantes:** *Students* (estudantes de graduação em Engenharia de Software), caracterizando desenvolvedores novatos.
*   **Problema:** *Toy problem* (mini-projetos individuais com escopo fechado para viabilizar a execução em tempo limitado).
*   **Especificidade:** *Specific* (focado na linguagem Java e framework JUnit 5).
*   **Processo e Ferramentas:** Uso de IDE VSCode, controle de versão via Git/GitHub e coleta manual de tempo. Haverá um treinamento de nivelamento (instrumentação) para mitigar a falta de conhecimento prévio.

## **2.3 Trabalhos e Evidências Prévias**
*   **Beck (2003) – *Test-Driven Development: By Example*:** Obra seminal que estabelece o ciclo *Red-Green-Refactor* e sugere melhoria no design (atributo interno) e redução de defeitos (atributo externo).
*   **Nagappan et al. (2008):** Estudo de caso industrial na Microsoft e IBM indicando aumento significativo de qualidade (redução de 40-90% em defeitos), porém com aumento de 15-35% no tempo de desenvolvimento (redução de produtividade).
*   **Rafique & Mišić (2013):** Meta-análise indicando que os efeitos do TDD na qualidade são mais fortes em projetos pequenos e acadêmicos do que em industriais, mas a produtividade tende a cair.

## **2.4 Referencial Teórico e Empírico**
O estudo baseia-se na comparação entre o desenvolvimento *Test-Last* (tradicional) e *Test-First* (TDD).

**Atributos e Métricas Selecionadas (Baseado em ISO/IEC 25010 e GQM):**

1.  **Atributos Internos (Produto):**
    *   *Cobertura de Testes:* Percentual de *statements* cobertos (medida de qualidade do teste, não necessariamente do software).
    *   *Tamanho:* Medido em LOC (*Lines of Code*) da solução (excluindo testes e comentários).

2.  **Atributos Externos (Qualidade em Uso):**
    *   *Confiabilidade Funcional:* Mensurada pela **Densidade de Defeitos** (Número de falhas em testes de aceitação / Tamanho).

3.  **Atributos de Recurso/Processo:**
    *   *Esforço:* Tempo total (em minutos) para completar a tarefa.
    *   *Produtividade:* Calculada como uma medida derivada: `Produtividade = Tamanho / Esforço`.

**Hipóteses Preliminares:**
*   A técnica TDD aumenta a confiabilidade (reduz a densidade de defeitos) em comparação à abordagem tradicional (**H1**).
*   A técnica TDD reduz a produtividade (LOC/hora) de desenvolvedores novatos devido à sobrecarga cognitiva da criação dos testes (**H2**).
   
**Considerações metodológicas:**

  * Defeitos serão contabilizados por meio de revisão estruturada e execução de testes independentes.
  * Cobertura de testes será utilizada como métrica complementar de qualidade, não como substituto da detecção de defeitos.







