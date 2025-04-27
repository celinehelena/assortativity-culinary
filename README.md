# Trabalho 2 - Análise de Assortatividade em Grafos de Ingredientes da Culinária Brasileira

Este trabalho repositório contém a implementação do trabalho da disciplina de Algoritmos e Estrutura de dados 2, cujo objetivo é construir um grafo de co-ocorrência de ingredientes a partir de 50 receitas populares da culinária brasileira e analisar a assortatividade do grafo com base na classificação dos ingredientes.

## Responsável
- Celine Helena Abrantes de Andrade. Matrícula: 20200078207.

---

## Estrutura do repositório
- `images/` — Pasta contendo imagens geradas durante o trabalho.
- `Ingredientes.csv ` — Arquivo com os dados organizados.
- `Ingredientes.ipynb` —  Arquivo com o código usado.
- `README.md` — Este documento.
- `llm_info.md` — Arquivo com os prompt(s) utilizados para identificar ingredientes.

---
## Análise da Rede de Ingredientes

Para a realização da atividade, foi necessário construir um grafo de co-ocorrência a partir de 50 receitas populares da culinária brasileiro usando um modelo de linguagem (Gemini AI) para baseado em uma imagem da receita ser gerado a descrição dos ingredientes do prato e classificá-los nas categorias: Proteína, Carboidrato, Vegetal, Fruta,Laticínio, Gordura, Condimento, Outro. Sendo organizando em um arquivo de extensão .csv da seguinte forma:
- nome_receita
- ingredientes
- tipo_ingredientes

O grafo foi construido tendo os nós como sendo ingredientes, as arestas, as ligações ente ingredientes que aparecem na mesma receita, e os atributos dos nós, o tipo de ingrediente.

Com o grafo gerado, calculou-se o coeficiente de assortatividade da rede, utilizando a **categoria do ingrediente** como o atributo principal dos nós. E o resultado obtido foi um coeficiente de valor negativo(-0.0556),indicando que o grafo é **disassortativo** (ou heterofílica) em relação à categoria dos ingredientes. Ou seja, os ingredientes tendem a se conectar (aparecer juntos na mesma receita) com ingredientes de categorias *diferentes* com mais frequência do que com ingredientes da *mesma* categoria. Este é um resultado bastante esperado para receitas culinárias devido a se optar por pratos equilibrados em que se busca combinar diferentes tipos de alimentos: uma fonte de proteína (carne, ovos) com um carboidrato (arroz, farinha, mandioca), vegetais para sabor e nutrientes, gorduras para cozimento e sabor, e condimentos para tempero. 

A visualização da rede foi gerada utilizando um **diagrama de cordas (chord diagram)**, onde observa-se uma densa rede de conexões (cordas) ligando **arcos de cores diferentes** e a estrutura é dominada pelas interações *entre* os diferentes grupos, conforme mostra a imagem. Por exemplo, é perceptível fortes conexões entre:
    *   Proteína <-> Vegetal
    *   Proteína <-> Carboidrato
    *   Vegetal <-> Condimento
    *   Laticínio <-> Carboidrato (em sobremesas/pães)

---

## Vídeo explicativo
🎥 [Link para o vídeo no Loom ou YouTube](https://youtu.be/N20GzhttK9o)
## Referências

- NetworkX documentation: https://networkx.org/
- Gemini Ai: https://gemini.google.com/
