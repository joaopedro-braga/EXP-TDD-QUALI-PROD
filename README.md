# Plano de Experimento – Scoping e Planejamento

# **1. Identificação Básica**

## **1.1 Título do Experimento**

**Avaliação do Impacto da Técnica Test-Driven Development (TDD) na Qualidade e Produtividade de Desenvolvedores de Software**

## **1.2 ID / Código**

EXP-TDD-QUALI-PROD-2025

## **1.3 Versão e Histórico**

| Versão | Data       | Descrição                                                                                                                                  |
| ------ | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| v1.0   | 20/11/2025 | Versão inicial do plano (Identificação Básica, Contexto e Problema)                                                                        |
| v1.1   | 25/11/2025 | Versão preliminar (Inclusão do Escopo, Objetivo, Stakeholders/Impacto, Riscos de alto nível, Premissas e Critérios de Sucesso)             |


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


---

# Plano de Experimento – Entrega 2

# **3. Objetivos e Questões (Goal / Question / Metric)**

## **3.1 Objetivo Geral (Template de Escopo)**

O objetivo do experimento foi definido utilizando o template padrão de definição de escopo:

| Campo | Definição |
| :--- | :--- |
| **Analyze (Analisar)** | A técnica de desenvolvimento *Test-Driven Development* (TDD) em comparação ao desenvolvimento tradicional (*Test-Last*). |
| **For the purpose of (Com o propósito de)** | **Avaliar** e caracterizar o impacto técnico e humano. |
| **With respect to (Com relação a)** | Sua **eficácia** (qualidade externa e interna) e **eficiência** (produtividade). |
| **From the point of view of (Do ponto de vista de)** | Do **pesquisador** e de **educadores** de Engenharia de Software. |
| **In the context of (No contexto de)** | Estudantes de graduação (desenvolvedores novatos) resolvendo problemas de lógica em Java (*Toy Problems*). |

---

## **3.2 Objetivos Específicos, Questões e Métricas (GQM)**

Abaixo, o desdobramento do objetivo geral utilizando o framework GQM. Foram definidos 4 objetivos específicos, cada um com 3 questões de pesquisa e suas respectivas métricas.

| Objetivo Específico | Questões de Pesquisa (Questions) | Métricas Associadas (Metrics) |
| :--- | :--- | :--- |
| **O1. Avaliar a confiabilidade funcional (Qualidade Externa)** | **Q1.1** O uso de TDD reduz a quantidade absoluta de falhas no software entregue? | **M1.** Número de Falhas (Defect Count)<br>**M2.** Densidade de Defeitos |
| | **Q1.2** A solução desenvolvida com TDD passa em mais casos de teste de aceitação? | **M3.** Taxa de Aceitação de Testes<br>**M4.** Completude Funcional |
| | **Q1.3** Qual a gravidade dos defeitos que permanecem no código entregue? | **M1.** Número de Falhas<br>**M5.** Índice de Severidade Média |
| **O2. Avaliar a qualidade estrutural do código (Qualidade Interna)** | **Q2.1** O TDD influencia na complexidade lógica (caminhos independentes) do código? | **M6.** Complexidade Ciclomática<br>**M7.** Tamanho do Código (LOC) |
| | **Q2.2** O TDD incentiva uma maior cobertura de testes automatizados pelos alunos? | **M8.** Cobertura de Código (Code Coverage)<br>**M9.** Número de Asserções |
| | **Q2.3** O código produzido tende a ser mais modular (menores métodos)? | **M7.** Tamanho do Código (LOC)<br>**M10.** Número de Métodos por Classe |
| **O3. Avaliar a eficiência e produtividade do processo** | **Q3.1** Quanto tempo a mais (ou a menos) é gasto desenvolvendo com TDD? | **M11.** Esforço Total (Tempo)<br>**M12.** Produtividade (LOC/Hora) |
| | **Q3.2** Existe uma correlação diferente entre tamanho e esforço nas duas técnicas? | **M7.** Tamanho do Código (LOC)<br>**M11.** Esforço Total (Tempo) |
| | **Q3.3** O tempo gasto corrigindo erros (*rework*) é menor com TDD? | **M13.** Tempo de *Rework* (Correção)<br>**M1.** Número de Falhas |
| **O4. Avaliar a percepção subjetiva do desenvolvedor** | **Q4.1** Qual técnica foi percebida como mais difícil de aplicar pelos alunos? | **M14.** Nível de Dificuldade Percebida<br>**M15.** Carga Cognitiva Percebida |
| | **Q4.2** Os alunos sentem mais confiança na corretude do código feito com TDD? | **M16.** Nível de Confiança<br>**M13.** Tempo de *Rework* (Correção) |
| | **Q4.3** Há intenção de uso futuro da técnica aprendida em projetos profissionais? | **M17.** Intenção de Adoção<br>**M14.** Nível de Dificuldade Percebida |

---

## **3.3 Definição das Métricas e Unidades**

A tabela abaixo descreve todas as métricas identificadas no GQM, suas unidades de medida e classificação.

| ID | Nome da Métrica | Descrição | Unidade |
| :--- | :--- | :--- | :--- |
| **M1** | Número de Falhas | Quantidade absoluta de falhas detectadas pela suíte de testes de aceitação (gabarito) do professor. | Inteiro (contagem) |
| **M2** | Densidade de Defeitos | Razão entre o número de falhas e o tamanho do código (M1 / M7). | Falhas / KLOC |
| **M3** | Taxa de Aceitação | Percentual de casos de teste de aceitação (caixa-preta) que passaram com sucesso. | Porcentagem (%) |
| **M4** | Completude Funcional | Número de requisitos obrigatórios implementados corretamente conforme especificação. | Inteiro |
| **M5** | Índice de Severidade | Média ponderada da gravidade das falhas encontradas (escala: 1=Cosmético a 5=Crítico). | Real (1.0 a 5.0) |
| **M6** | Complexidade Ciclomática | Número de caminhos linearmente independentes no código fonte (Métrica de McCabe). | Inteiro |
| **M7** | Tamanho do Código (LOC) | Linhas de código físico executável (*Non-Commented Lines of Code*). | LOC |
| **M8** | Cobertura de Código | Porcentagem de linhas de código de produção executadas pela suíte de testes unitários criada pelo aluno. | Porcentagem (%) |
| **M9** | Número de Asserções | Contagem total de comandos de verificação (`assert`) nos testes unitários. | Inteiro |
| **M10** | Métodos por Classe | Quantidade de métodos definidos na classe principal da solução. | Inteiro |
| **M11** | Esforço Total | Tempo decorrido entre o início da leitura do problema e a submissão final. | Minutos |
| **M12** | Produtividade | Razão entre o tamanho do software produzido e o esforço gasto (M7 / M11). | LOC / Hora |
| **M13** | Tempo de *Rework* | Tempo gasto especificamente corrigindo bugs após a primeira tentativa de execução/falha. | Minutos |
| **M14** | Dificuldade Percebida | Autoavaliação sobre quão difícil foi utilizar a técnica proposta. | Escala Ordinal (1-5) |
| **M15** | Carga Cognitiva | Autoavaliação do esforço mental exigido durante a tarefa. | Escala Ordinal (1-10)|
| **M16** | Nível de Confiança | Autoavaliação sobre a confiança de que o código não possui bugs. | Escala Ordinal (1-5) |
| **M17** | Intenção de Adoção | Probabilidade subjetiva de utilizar a técnica em projetos futuros. | Escala Ordinal (1-5) |

---

# **4. Escopo e Contexto do Experimento**

## **4.1 Escopo Funcional e de Processo**
*   **Incluído:** O experimento abrange as atividades de codificação, criação de testes unitários (utilizando o framework JUnit), refatoração de código e correção de defeitos. O domínio do problema será estritamente algorítmico, envolvendo lógica de programação.
*   **Excluído:** Atividades de levantamento e análise de requisitos (os requisitos serão fornecidos prontos), design de interface gráfica (a interação será via linha de comando ou chamada de função), configuração de ambiente (será padronizado) e *deployment*.

## **4.2 Contexto do Estudo**
*   **Ambiente:** *Off-line* (laboratório acadêmico controlado).
*   **Participantes:** Estudantes de graduação em Engenharia de Software, caracterizando desenvolvedores novatos.
*   **Tarefa:** Problema de "brinquedo" (*toy problem*) com escopo fechado e baixa complexidade de domínio, viável de ser realizado em tempo limitado.
*   **Tecnologia:** Linguagem Java e IDE VSCode.

## **4.3 Premissas**
1.  Os alunos possuem conhecimentos prévios suficientes em Java e Orientação a Objetos para realizar a tarefa.
2.  Os alunos reportarão o tempo de esforço com honestidade.
3.  As máquinas do laboratório possuem a mesma configuração de hardware e software, não influenciando no desempenho.

## **4.4 Restrições**
1.  **Tempo:** O experimento deve ser executado em uma janela única de 100 minutos (duração da aula).
2.  **Amostra:** O número máximo de participantes é limitado aos alunos matriculados na disciplina (estimado entre 20 e 30).
3.  **Custo:** Não há orçamento para ferramentas pagas; devem ser usadas apenas ferramentas *open-source*.

## **4.5 Limitações Previstas**
*   **Validade Externa:** Devido ao uso de estudantes e problemas pequenos, os resultados podem não ser generalizáveis para ambientes industriais com sistemas legados e equipes experientes.
*   **Efeito de Aprendizado:** Pode haver uma curva de aprendizado inicial com a ferramenta de testes que afete a produtividade no grupo TDD.

---

# **5. Stakeholders e Impacto Esperado**

## **5.1 Stakeholders Principais**
1.  **Pesquisador (Aluno):** Responsável pelo planejamento, execução e análise.
2.  **Professor Orientador:** Interessado na integridade metodológica.
3.  **Participantes (Alunos da disciplina):** Sujeitos do experimento.

## **5.2 Interesses e Expectativas**
*   **Pesquisador:** Espera coletar dados suficientes para validar as hipóteses e concluir o TCC.
*   **Professor:** Espera que o experimento sirva como atividade didática de fixação de conteúdo.
*   **Alunos:** Esperam aprender uma técnica nova (TDD) e que a participação conte como horas complementares ou nota de participação.

## **5.3 Impactos Potenciais**
*   **No Processo de Ensino:** O experimento consumirá uma aula inteira, exigindo ajuste no cronograma da disciplina.
*   **Nos Participantes:** Possível frustração inicial com a técnica TDD se o treinamento prévio não for eficaz, o que pode impactar a motivação.

---

# **6. Riscos de Alto Nível, Premissas e Critérios de Sucesso**

## **6.1 Riscos de Alto Nível**
1.  **Mortalidade dos Sujeitos:** Alunos desistirem no meio da tarefa ou não submeterem o código final.
2.  **Viés de Comunicação:** Alunos trocarem informações sobre a solução durante o experimento.
3.  **Falha Técnica:** Problemas com a IDE ou plugin de testes nas máquinas do laboratório no dia da execução.

## **6.2 Critérios de Sucesso Globais (Go / No-Go)**
*   **Go:** Obtenção de pelo menos 16 pontos de dados válidos (códigos compiláveis e tempos registrados).
*   **Go:** Execução completa do protocolo sem interrupções externas graves (ex: queda de energia).

## **6.3 Critérios de Parada Antecipada**
*   Se o número de participantes presentes for inferior a 10 (impossibilita análise estatística).
*   Se houver falha generalizada de infraestrutura (internet ou repositório) que impeça o acesso ao enunciado ou o envio da solução.




