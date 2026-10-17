# IE 521 – Tecnologia de Circuitos Integrados
**Prof. Diniz / Prof. Manera / Prof. Puydinger**  
**Exercício – Transistor MOS**

---

## Q1. Sequência Básica de Fabricação

Deseja-se projetar um transistor MOS, utilizando-se os simuladores Athena e Atlas da Silvaco, a partir da sequência básica de fabricação a seguir:

**Lâmina:** Silício tipo **A**, com dopagem **B**.

1. Deposição de 500 nm de óxido de silício.
2. **Fotogravação 1** – abertura da região ativa.
3. Oxidação térmica de porta de 20 nm em 900 ºC e 40 minutos (corrigir o tempo se for o caso).
4. Implantação Iônica para ajuste de tensão de limiar com energia de 30 keV.
5. *(Etapa a ser adicionada para as questões Q2 e Q3)*.
6. Deposição de Silício policristalino intrínseco (400 nm) em 600 ºC e 15 minutos.
7. Difusão de **C** para dopagem degenerada do silício policristalino de porta.
8. **Fotogravação 2** – definição do silício policristalino.
9. Implantação de **D** de Fonte/Dreno com energia **E** e dose **F**.
10. Recozimento em forno com ambiente de N2 em 940 ºC e 20 minutos para ativação das impurezas implantadas.
11. Deposição de 400 nm de óxido de silício.
12. Densificação do óxido em forno com ambiente de N2 em 940 ºC e 10 minutos.
13. **Fotogravação 3** – abertura de contatos.
14. Deposição de 100 nm de Titânio (barreira de difusão).
15. Deposição de 1000 nm de Alumínio.
16. **Fotogravação 4** – definição do Alumínio e Titânio.
17. Sinterização em 420 ºC e 30 minutos.

> **Obs.:** As variáveis **A, B, C, D, E** e **F** são fornecidas de acordo com a tabela de projetos.

### Itens da Q1:

* **a.** Desenhe o perfil do transistor MOS após as etapas 4, 9, 13 e 17.
* **b.** Projete a etapa 4 (dose de implantação e o tipo de dopante necessário) para se ter tensão de limiar de transistor de canal longo (L = 5 µm e W = 10 µm) em módulo de 0.8 V (Vtn = +0.8 V ou Vtp = -0.8 V) para tensão de dreno VDS de 0.1 V em módulo. Adote o número de cargas de interface SiO2/Si = 1x10^11 cm^-2.
* **c.** Determine o efeito de canal curto na tensão de limiar traçando a curva Vt x L para L = 0.4, 0.6, 0.8, 1.0, 1.2, 2.0 e 5.0 µm. Explique os resultados obtidos. Qual seria o efeito da espessura de óxido e da profundidade de junção sobre esta curva?
* **d.** Determine o comprimento de canal L para o qual a tensão de perfuração MOS (*punchthrough*) seja 10 V em módulo (utilize o critério da Dra. Sally Liu, ou seja, onde a corrente IDS = 10^-9 * W / L, com VGS = VFB).
* **e.** Elabore curvas:
  * **a)** log(IDS) x VGS para VDS de 1 a 5 V;
  * **b)** distribuição bidimensional de densidade de elétrons e de potencial elétrico no transistor para VDS = 5 V e VGS = 0 V para W = 10 µm, L = 0.6 µm.
* **f.** Gere as curvas características, IDS x VDS (0 a 5 V) tendo VGS como parâmetro (0 a 5 V) para o transistor fabricado com W = 10 µm, L = 0.6 µm.

---

## Q2. Inclusão da Etapa 5 (Ajuste de Punchthrough)

Seguindo as etapas de processo da questão Q1, adicione a **etapa 5** do processo para o transistor com W = 10 µm, L = 0.6 µm:

5. Implantação Iônica para ajuste de *punchthrough*, com energia de 160 keV. Ajuste o valor da dose para que não ocorra perfuração MOS.

### Itens da Q2:

* **a.** Curvas log(IDS) x VGS para VDS de 1 a 5 V.
* **b.** Distribuição bidimensional de densidade de elétrons e potencial elétrico no transistor para VDS = 5 V e VGS = 0 V.
* **c.** Curvas características, IDS x VDS (0 a 5 V) parametrizado por VGS (0 a 5 V).

---

## Q3. Adição do LDD (Lightly Doped Drain)

Acrescentar à sequência de fabricação da questão Q2 (transistor otimizado) as seguintes etapas de processo:

* **8.1.** Implantação Iônica de **G** para formação de LDD com energia **H** e dose de 1x10^13 cm^-2.
* **8.2.** Deposição de 300 nm de óxido de silício.
* **8.3.** Remoção de óxido por plasma (formação de um espaçador – *Spacer* – de 0.25 µm de comprimento).

### Itens da Q3:

* **a.** Desenhar o perfil do transistor após as etapas 8.1, 9 e 17.
* **b.** Obter a nova curva Vt x L. Comparando com a curva obtida no item **c** da Q1, qual sequência de fabricação apresenta melhor desempenho com relação ao efeito de canal curto na tensão de limiar? Explique.
* **c.** Determine em que posição do canal do transistor o campo elétrico lateral é maior. Comparando-se o transistor **COM** e **SEM** LDD, qual deles apresenta menor campo elétrico máximo? Explique através de simulações.

---

## Tabela de Variáveis dos Projetos

| VARIÁVEIS | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **A** | P | P | P | P | N | N | N | N |
| **B [10^15 cm^-3]** | 1 | 4 | 6 | 8 | 2 | 4 | 6 | 8 |
| **C** | FOS | BOR | FOS | BOR | FOS | BOR | FOS | BOR |
| **D** | FOS | FOS | FOS | FOS | BOR | BOR | BOR | BOR |
| **E [keV]** | 40 | 50 | 50 | 60 | 20 | 20 | 20 | 20 |
| **F [10^15 cm^-2]** | 7 | 8 | 4 | 4 | 8 | 8 | 4 | 4 |
| **G** | FOS | FOS | FOS | FOS | BOR | BOR | BOR | BOR |
| **H [keV]** | 30 | 30 | 30 | 30 | 10 | 10 | 10 | 10 |

> **Legenda:** **FOS** = FÓSFORO; **BOR** = BORO
