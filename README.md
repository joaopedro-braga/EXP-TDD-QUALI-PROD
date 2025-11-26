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
| v1.2   | 25/11/2025 | Versão preliminar (Inclusão do Modelo conceitual e hipóteses; Variáveis, fatores, tratamentos e objetos de estudo; Desenho experimental)   |
| v1.3   | 26/11/2025 | Versão preliminar (Inclusão da População, sujeitos e amostragem; Instrumentação e protocolo operacional; Plano de análise de dados (pré-execução))   |


## **1.4 Datas**

* Data de criação: **20/11/2025**
* Última atualização: **26/11/2025**

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


---

# **7. Modelo Conceitual e Hipóteses**

## **7.1 Modelo Conceitual do Experimento**
O modelo conceitual baseia-se na premissa de que a técnica de desenvolvimento (Fator) influencia diretamente as variáveis de resposta relacionadas à qualidade e produtividade.

A teoria sugere que o ciclo *Red-Green-Refactor* do TDD impõe uma carga cognitiva inicial maior e exige a escrita de mais linhas de código (testes), o que tende a reduzir a produtividade imediata (velocidade de escrita). Por outro lado, essa abordagem força a análise de casos de borda antes da implementação e promove a refatoração contínua, o que teoricamente reduz a densidade de defeitos e melhora a estrutura interna do código.

**Esquema Causal:**
*   **Variável Independente (Causa):** Técnica de Desenvolvimento (TDD vs. Tradicional).
*   **Variáveis Dependentes (Efeitos):**
    *   *Qualidade Externa:* Densidade de Defeitos.
    *   *Qualidade Interna:* Complexidade Ciclomática.
    *   *Produtividade:* LOC/Hora.
    *   *Aspecto Humano:* Dificuldade Percebida.

## **7.2 Hipóteses Formais**

Para garantir a cobertura dos objetivos definidos no GQM, foram formalizadas hipóteses para cada uma das principais dimensões de análise (Qualidade Externa, Qualidade Interna, Produtividade e Percepção).

**Hipótese 1: Qualidade Externa (Ref. O1 do GQM)**
*Investiga se o TDD reduz a incidência de erros.*
*   **H0₁ (Nula):** Não há diferença significativa na densidade de defeitos entre o código desenvolvido com TDD e o desenvolvido com a abordagem tradicional.
    *   $\mu_{TDD\_Defeitos} = \mu_{Trad\_Defeitos}$
*   **H1₁ (Alternativa):** A densidade de defeitos no código desenvolvido com TDD é menor do que na abordagem tradicional.
    *   $\mu_{TDD\_Defeitos} < \mu_{Trad\_Defeitos}$

**Hipótese 2: Qualidade Interna (Ref. O2 do GQM)**
*Investiga se o TDD resulta em código menos complexo (mais simples).*
*   **H0₂ (Nula):** Não há diferença significativa na Complexidade Ciclomática média dos métodos entre as duas técnicas.
    *   $\mu_{TDD\_Complexidade} = \mu_{Trad\_Complexidade}$
*   **H1₂ (Alternativa):** A Complexidade Ciclomática no código desenvolvido com TDD é menor do que na abordagem tradicional.
    *   $\mu_{TDD\_Complexidade} < \mu_{Trad\_Complexidade}$

**Hipótese 3: Produtividade (Ref. O3 do GQM)**
*Investiga o impacto na velocidade de desenvolvimento.*
*   **H0₃ (Nula):** Não há diferença significativa na produtividade (LOC/hora) entre desenvolvedores usando TDD e abordagem tradicional.
    *   $\mu_{TDD\_Prod} = \mu_{Trad\_Prod}$
*   **H1₃ (Alternativa):** A produtividade dos desenvolvedores usando TDD é menor do que a dos que usam a abordagem tradicional (devido ao esforço extra de escrever testes).
    *   $\mu_{TDD\_Prod} < \mu_{Trad\_Prod}$

**Hipótese 4: Percepção do Desenvolvedor (Ref. O4 do GQM)**
*Investiga a dificuldade sentida pelos alunos.*
*   **H0₄ (Nula):** Não há diferença na percepção de dificuldade entre usar TDD ou a abordagem tradicional.
    *   $\mu_{TDD\_Dificuldade} = \mu_{Trad\_Dificuldade}$
*   **H1₄ (Alternativa):** A percepção de dificuldade é maior no grupo TDD (devido à curva de aprendizado para novatos).
    *   $\mu_{TDD\_Dificuldade} > \mu_{Trad\_Dificuldade}$

## **7.3 Nível de Significância**
Será adotado um nível de significância **$\alpha = 0.05$** (5%) para todos os testes de hipótese. Isso estabelece o limite para rejeição da hipótese nula.

---

# **8. Variáveis, Fatores, Tratamentos e Objetos de Estudo**

## **8.1 Objetos de Estudo**
O objeto de estudo será a tarefa de programação que os participantes deverão resolver. Será utilizado um problema algorítmico de escopo fechado (ex: "Conversor de Números Romanos"), que permite isolar a técnica de codificação de outras variáveis como levantamento de requisitos.

## **8.2 Sujeitos / Participantes**
Os sujeitos são estudantes de graduação em Engenharia de Software. Eles representam uma população de desenvolvedores em formação, com conhecimento prévio em Java, mas pouca experiência prática em processos industriais.

## **8.3 Tabela de Variáveis**

A tabela abaixo descreve todas as variáveis envolvidas no experimento, mapeadas para as hipóteses acima.

| Variável | Tipo | Escala | Descrição | Unidade |
| :--- | :--- | :--- | :--- | :--- |
| **Técnica de Desenvolvimento** | Independente (Fator) | Nominal | A abordagem utilizada para construir o software. | Categoria (TDD/Trad) |
| **Densidade de Defeitos** | Dependente (H1) | Razão | Quantidade de falhas funcionais normalizada pelo tamanho do código. | Falhas/KLOC |
| **Complexidade Ciclomática** | Dependente (H2) | Razão | Medida de caminhos independentes no código (McCabe). | Inteiro |
| **Produtividade** | Dependente (H3) | Razão | Velocidade de produção de código funcional entregue. | LOC/Hora |
| **Dificuldade Percebida** | Dependente (H4) | Ordinal | Autoavaliação da dificuldade da tarefa. | Escala Likert (1-5) |
| **Experiência em Java** | Controle | Ordinal | Nível declarado de conhecimento na linguagem. | Escala Likert (1-5) |
| **Ambiente de Desenv.** | Controle | Nominal | IDE, versão do JDK e Sistema Operacional utilizados. | N/A |

## **8.4 Fatores e Tratamentos**

O experimento manipula um único fator com dois níveis (tratamentos).

| Fator | Tratamento (Nível) | Descrição Operacional |
| :--- | :--- | :--- |
| **Técnica de Desenvolvimento** | **T1: TDD (Test-Driven Development)** | O participante deve escrever o teste unitário antes de escrever o código de produção (*Test-First*), seguindo ciclos curtos de iteração. |
| | **T2: Tradicional (Test-Last)** | O participante escreve o código de produção primeiro e, opcionalmente, escreve testes ao final ou realiza testes manuais. |

---

# **9. Desenho Experimental**

## **9.1 Tipo de Desenho**
Será utilizado um desenho de **Um Fator com Dois Tratamentos** (*One factor with two treatments*), organizado de forma **Completamente Randomizada**.
Este design é adequado para comparar as médias das variáveis dependentes entre dois grupos distintos (Grupo TDD vs. Grupo Controle), simplificando a execução em sala de aula e evitando o efeito de aprendizado que ocorreria se o mesmo aluno resolvesse o problema duas vezes.

## **9.2 Randomização e Alocação**
A alocação dos sujeitos aos tratamentos será aleatória para distribuir homogeneamente as variações individuais (como talento ou experiência prévia).
1.  Identificação de todos os participantes elegíveis.
2.  Uso de um gerador de números aleatórios para atribuir cada participante ao Grupo A ou Grupo B.
3.  Verificação pós-alocação para garantir que não houve concentração acidental de alunos experientes em um único grupo (se houver, realizar novo sorteio).

## **9.3 Balanceamento**
O experimento buscará ser balanceado, visando ter o mesmo número de observações em cada tratamento ($n_A = n_B$). O balanceamento aumenta a robustez do teste estatístico contra desvios de normalidade e homogeneidade de variância.

## **9.4 Número de Grupos e Sessões**
*   **Grupos:** 2 Grupos (Entre-Sujeitos).
*   **Sessões:** 1 Sessão única.
    *   Todos os participantes executarão o experimento simultaneamente no mesmo laboratório para garantir controle sobre variáveis ambientais (tempo disponível, instruções fornecidas, ruído, temperatura).

---

# **10. População, Sujeitos e Amostragem**

## **10.1 População-Alvo**
A população-alvo deste estudo compreende **desenvolvedores de software novatos** ou em formação acadêmica. Especificamente, busca-se representar estudantes de graduação em cursos de computação que já possuam conhecimentos fundamentais de programação orientada a objetos e testes unitários, mas que ainda não tenham consolidado práticas industriais avançadas.

## **10.2 Critérios de Inclusão**
Para participar do experimento, o sujeito deve atender aos seguintes critérios:
1.  Estar regularmente matriculado na disciplina de Engenharia de Software ou correlata.
2.  Possuir conhecimento prévio da linguagem Java (nível básico a intermediário).
3.  Ter participado do treinamento de nivelamento sobre JUnit oferecido previamente.
4.  Assinar o Termo de Consentimento Livre e Esclarecido (TCLE).

## **10.3 Critérios de Exclusão**
Serão desconsiderados os dados de participantes que:
1.  Não entregarem o código fonte final compilável (erro de sintaxe impeditivo).
2.  Não preencherem os logs de tempo ou os questionários de percepção.
3.  Declararem, no questionário demográfico, nunca ter escrito um teste unitário anteriormente (falta de *skill* mínima para a tarefa).

## **10.4 Tamanho da Amostra e Seleção**
*   **Tamanho Planejado:** Estima-se um total de **24 a 30 participantes**, divididos igualmente entre os dois grupos (12 a 15 por tratamento). Embora amostras pequenas reduzam o poder estatístico, este número é compatível com o tamanho médio de turmas acadêmicas e suficiente para detectar tamanhos de efeito médios a grandes.
*   **Método de Seleção:** A amostragem será por **conveniência** (alunos disponíveis na instituição), porém a alocação aos grupos (TDD vs. Tradicional) será **aleatória (randomizada)** para mitigar vieses de seleção.

---

# **11. Instrumentação e Protocolo Operacional**

## **11.1 Instrumentos de Coleta**
Os seguintes artefatos serão utilizados para garantir a execução e a coleta de dados:

1.  **Questionário de Caracterização:** Formulário online para coletar dados demográficos e nível de experiência em Java e Testes (Variável de Controle).
2.  **Especificação da Tarefa:** Documento PDF contendo os requisitos funcionais do "Kata de Programação" (ex: Conversor de Números Romanos), com exemplos de entrada e saída.
3.  **Ambiente de Desenvolvimento (IDE):** VSCode configurado com JDK 17 e biblioteca JUnit 5 pré-instalada.
4.  **Repositório de Código (Template):** Um repositório Git contendo a estrutura básica do projeto (scaffold) para garantir que todos comecem do mesmo ponto.
5.  **Planilha de Log de Tempo:** Planilha simples onde o aluno registrará a hora de início e fim (Métrica M11).
6.  **Questionário Pós-Experimento:** Formulário contendo escalas Likert para avaliar Dificuldade Percebida (M14), Confiança (M16) e Carga Cognitiva (NASA-TLX simplificado - M15).
7.  **Suíte de Testes de Aceitação (Gabarito):** Conjunto de testes automatizados criados pelo pesquisador, ocultos aos alunos, para medir a Completude Funcional (M4) e o Número de Falhas (M1).

## **11.2 Fluxograma do Experimento**

Abaixo, o fluxo operacional detalhado do experimento, demonstrando a interação entre stakeholders, instrumentos e a geração das métricas.

![Fluxograma do Experimento](https://www.plantuml.com/plantuml/png/XLDDRzn63BthLn3eHGPI84RQj50EZRmVgGkxTknjJxdG4dUNoMYeScOCjqr_ZD53q08z-IVeZvMZbHlNmCANnOgatdjwZtmT8cfCdIl21_OzAdQ0JUHhZh_2xmN04JOVDYh9jpDnel35Sh5Sp1Qv8zgIJjNws-VFNxmi_YYAZ-SKVaaSiBLwUQPCFkR_1n-BaQkevhHcpmhdqYU7mwVXJm62cN8S_bAMyAgepfMo5eLZlrQa43N5fFZEboTuzGoEvulm32webs0ltIaBlE5uy2gp6mKttAEF16NjaXTZhkeGs1lUYhGJQ8rEV31btDcFx1Z9DrjIU9kCZyKFjuPh0WmDdJ7_ZCh3xJMv_6vKSLJ1ugOdg_xjRMQat__nrKh996I-KS2FR52xHmF_uIVF4KPP3N6K0Alvt12h2_IjTFpRv5DhdSlqFe-OJruYWV9c6osFsaapJTMESFG5AskyqTHR3SeC2PB-AnrPIR7bXiMZEoZ8jv0XYuBNKBvDw41sezyTGDoIXtB2gaPv1bGT-npEI6jsX4RfcXIYMKZlV0uXc6PeXhkMDs9yrlXooHfoMkG2tKCULV1Gotxe2Ue1-4WsGP_W3jctlDw_3HVKq1MfWVRKy9hlVMiHLgYqpejsTlMUngHiAgPMSXYB6sfIH9scSlDSPQFOxG0U9N8gdgFevynNrFLYZVBqy31_qbfq-2ImalW_-wlBTDLHD86NudO6c4qSdzemkqNAwcgDfYulKJaRtNeaFliLifuwxzeetVmqKHKiqMtHRklqXUM1D_Xm98FKTXQEmsZAS6lUZYPCB1dZPGKpwNf7DznYIuRqJKRgq6y5Jivc-uzq_mqksQDxvEtzDNA0EVLc7HbMleqS6rzZg780XrzLCCy19vVLZAMlJI7g1atdndEU_Upy4_Rw88xR1wSujrvuP0l6uPymEaCxgxD3ttC_t9b0ikaGfIzU6sVgtBy0)

## **11.3 Procedimento Experimental (Passo a Passo)**
1.  **Convite:** Os alunos serão convidados na semana anterior e informados sobre o objetivo pedagógico da atividade.
2.  **Nivelamento:** Uma aula de revisão de 30 minutos sobre JUnit será ministrada.
3.  **Setup:** No dia do experimento, os alunos acessam as máquinas e fazem login no formulário de coleta.
4.  **Execução:** Os alunos recebem o link do repositório. Ao iniciar, registram o horário.
    *   Grupo TDD segue o ciclo *Red-Green-Refactor*.
    *   Grupo Tradicional codifica livremente, testando ao final.
5.  **Encerramento:** Ao finalizar a tarefa (ou acabar o tempo limite de 90 minutos), o aluno faz o *commit/push*, registra o horário final e responde ao questionário de percepção.

---

# **12. Plano de Análise de Dados (Pré-execução)**

## **12.1 Tratamento dos Dados**
Antes da análise estatística, será realizada a limpeza dos dados:
*   **Sanity Check:** Códigos que não compilam serão descartados ou corrigidos minimamente (apenas imports) se o erro for trivial.
*   **Normalização:** Métricas de esforço serão convertidas para minutos. Métricas de tamanho (LOC) serão normalizadas para excluir linhas em branco e comentários (*Logical LOC*).
*   **Outliers:** Valores extremos de tempo (ex: alunos que terminaram em 5 minutos ou não terminaram) serão analisados via *Boxplot* e poderão ser removidos se indicarem falta de engajamento.

## **12.2 Estatística Descritiva**
Para cada grupo (TDD e Tradicional) e para cada uma das quatro variáveis dependentes (Defeitos, Complexidade, Produtividade, Dificuldade), serão calculadas as medidas de:
*   **Tendência Central:** Média e Mediana.
*   **Dispersão:** Desvio Padrão e Variância.

## **12.3 Teste de Hipóteses (Inferência)**
Para validar as quatro hipóteses definidas na etapa anterior, será seguido o fluxo de decisão abaixo para cada variável dependente:

1.  **Verificação de Normalidade:** Aplicação do teste de **Shapiro-Wilk** nos dados de cada grupo para cada métrica.
    *   Nível de significância para normalidade: $\alpha = 0.05$.

2.  **Seleção do Teste de Comparação:**
    *   **Se os dados forem Normais (Paramétricos):** Utilizar o **Teste t de Student para amostras independentes** (unicaudal, pois as hipóteses têm direção).
    *   **Se os dados NÃO forem Normais (Não-Paramétricos):** Utilizar o teste **Mann-Whitney U** (equivalente não-paramétrico do teste t).

3.  **Aplicação às Hipóteses:**

    *   **H1 (Qualidade Externa):** Teste estatístico sobre a *Densidade de Defeitos*. Espera-se média menor no TDD.
    *   **H2 (Qualidade Interna):** Teste estatístico sobre a *Complexidade Ciclomática*. Espera-se média menor no TDD.
    *   **H3 (Produtividade):** Teste estatístico sobre a variável *Produtividade (LOC/h)*. Espera-se média menor no TDD.
    *   **H4 (Percepção):** Teste estatístico sobre a variável ordinal *Dificuldade Percebida*. Como é uma escala Likert, o teste preferencial será o **Mann-Whitney U**.

4.  **Decisão:**
    *   Se o **p-valor < 0.05**, rejeita-se a Hipótese Nula (H0) correspondente, indicando diferença estatisticamente significativa.

## **12.4 Análise Qualitativa**
As respostas dos questionários abertos sobre a dificuldade da técnica serão analisadas por meio de codificação temática para identificar padrões (ex: "dificuldade em pensar no teste primeiro", "sensação de segurança ao refatorar"), servindo para explicar os resultados quantitativos de H4.

---

# **13. Avaliação de Validade (Ameaças e Mitigação)**

A validade de um experimento determina o quanto podemos confiar nos seus resultados e o quanto podemos generalizá-los. Abaixo, são analisadas as quatro principais categorias de validade, identificando ameaças específicas ao contexto deste estudo e as respectivas ações de mitigação planejadas.

## **13.1 Validade de Conclusão**
Refere-se à capacidade de tirar conclusões estatísticas corretas sobre a relação entre o tratamento e o resultado.

| Ameaça | Descrição no Contexto | Estratégia de Mitigação |
| :--- | :--- | :--- |
| **Baixo Poder Estatístico** | O tamanho da amostra (~24 alunos) pode ser insuficiente para detectar diferenças pequenas entre os grupos, levando a um Erro Tipo II (falso negativo). | Definir um nível de significância padrão ($\alpha=0.05$) e utilizar testes não-paramétricos (Mann-Whitney) caso a normalidade não seja atendida, pois são mais robustos para amostras pequenas. Aceitar conclusões apenas para tamanhos de efeito médios/grandes. |
| **Violação de Suposições** | Aplicar testes paramétricos (Teste t) em dados que não seguem distribuição normal (comum em métricas de software). | Realizar teste de normalidade (Shapiro-Wilk) antes da análise. Se a normalidade for violada, migrar automaticamente para testes não-paramétricos. |
| **Confiabilidade das Medidas** | Erros na coleta manual do tempo ou inconsistência na contagem de defeitos. | Automatizar a coleta de defeitos via suíte de testes (gabarito). Para o tempo, cruzar o registro manual do aluno com o *timestamp* do primeiro e último commit no Git. |

## **13.2 Validade Interna**
Refere-se à certeza de que foi o tratamento (TDD), e não outro fator, que causou o efeito observado.

| Ameaça | Descrição no Contexto | Estratégia de Mitigação |
| :--- | :--- | :--- |
| **Seleção (Selection)** | Alunos mais habilidosos podem acabar concentrados em um único grupo, distorcendo o resultado. | Utilizar alocação aleatória (randomização) para distribuir os níveis de habilidade. Verificar *a posteriori* se os grupos estão equilibrados usando os dados do questionário de experiência. |
| **Maturação (Maturation)** | Os alunos podem aprender a resolver o problema durante o experimento ou ficar cansados. | O experimento é curto (uma sessão), minimizando a maturação. A tarefa é inédita para evitar aprendizado prévio específico. |
| **Difusão do Tratamento** | Alunos do grupo TDD podem conversar com o grupo Tradicional e passar dicas da solução ou da técnica. | Realizar o experimento em sessão única e simultânea, com supervisão em sala para evitar comunicação entre os participantes. |
| **Desistência (Mortality)** | Alunos com dificuldade técnica podem desistir, deixando apenas os "melhores" na análise final. | Monitorar a sala durante a execução e oferecer suporte rápido para problemas de ambiente (IDE/Java), evitando desistência por frustração técnica (sem ajudar na lógica). |

## **13.3 Validade de Construto**
Refere-se à adequação das métricas escolhidas para representar os conceitos teóricos (Qualidade e Produtividade).

| Ameaça | Descrição no Contexto | Estratégia de Mitigação |
| :--- | :--- | :--- |
| **Mono-operação** | Usar apenas um único problema ("Toy Problem") pode não refletir a complexidade real de desenvolvimento de software. | Reconhecer essa limitação explicitamente. Escolher um problema (Kata) que envolva lógica não trivial para exigir raciocínio, e não apenas codificação mecânica. |
| **Viés de Medição** | Usar "Produtividade = LOC/Hora" pode premiar código verborrágico em vez de código eficiente. | Combinar a métrica de produtividade com a de qualidade (Defeitos). Código muito rápido mas cheio de bugs será penalizado na análise conjunta. |
| **Efeito do Experimentador** | Os alunos podem tentar "agradar" o professor usando TDD mesmo estando no grupo controle, ou forjar os testes depois. | O histórico de *commits* será analisado. Se um aluno do grupo TDD fizer *commits* gigantes de código sem testes prévios, será desclassificado ou realocado na análise. |

## **13.4 Validade Externa**
Refere-se à capacidade de generalizar os resultados para fora do experimento (para a indústria).

| Ameaça | Descrição no Contexto | Estratégia de Mitigação |
| :--- | :--- | :--- |
| **Interação Seleção-Tratamento** | Os sujeitos são estudantes, que podem não representar o comportamento de profissionais seniores (*Students vs Professionals*). | Limitar a generalização dos resultados para o contexto de "formação e treinamento de novos engenheiros" e "equipes júnior", evitando extrapolar para contextos críticos ou seniores. |
| **Interação Cenário-Tratamento** | O problema é pequeno e feito em laboratório (*Toy Problem*), diferente de sistemas reais com legado e dívida técnica. | Argumentar que o estudo foca na **mecânica da técnica** e no processo cognitivo inicial, que são melhor isolados em problemas pequenos. Sugerir replicação futura em projetos de disciplina maiores. |

## **13.5 Resumo das Ações Prioritárias**

Para garantir a integridade deste estudo, as seguintes ações são mandatórias:

1.  **Randomização Rigorosa:** Garantir que a divisão dos grupos seja feita por sorteio e não por escolha dos alunos (por exemplo, não deixar eles escolherem onde sentar se isso definir o grupo).
2.  **Protocolo de *Sanity Check*:** Antes de rodar a estatística, o pesquisador deve abrir aleatoriamente 20% dos repositórios para verificar se o grupo TDD realmente seguiu o ciclo (testes com timestamps anteriores ao código).
3.  **Transparência na Análise:** Reportar não apenas o *p-valor*, mas também o tamanho do efeito (*Effect Size*), para discutir a relevância prática dos achados, não apenas a significância estatística.


---


