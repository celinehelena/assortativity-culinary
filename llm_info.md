# Informações sobre o Modelo de Linguagem e Prompts Utilizados

## Modelo de Linguagem

O modelo de linguagem utilizado para a identificação e categorização dos ingredientes das receitas brasileiras foi o **Gemini Pro** (ou um modelo da família Gemini), desenvolvido pelo Google.

## Prompt(s) Utilizados

### Prompt Inicial (Definição da Tarefa)

O seguinte prompt foi fornecido inicialmente para definir a tarefa a ser realizada pelo modelo:

> Vou mandar 50 imagens de receitas populares da culinária brasileira e apartir delas gere os ingredientes do prato, no entanto não precisa dar a receita mas por exemplo se for uma feijoada é para ser feijão preto, carne de porco, arroz. Apenas os ingredientes que se classifiquem nas categorias: Proteína, leguminosa
> ■ Carboidrato
> ■ Vegetal
> ■ Fruta
> ■ Laticínio
> ■ Gordura
> ■ Condimento
> ■ Outro. Também classifique esses ingredientes nessas categorias. Irei mandar a imagens a seguir

### Interações Subsequentes (Envio das Imagens)

Após o prompt inicial, a interação seguiu o padrão abaixo para cada conjunto de imagens enviadas:

1.  **Usuário:** Enviava uma ou mais imagens de pratos brasileiros.
2.  **Usuário:** Fornecia o nome dos pratos correspondentes às imagens (ex: "pamonha, canjica e pao de queijo").
3.  **Modelo (Gemini):** Analisava cada imagem, identificava o prato com base no nome fornecido e na imagem, e listava os ingredientes principais, classificando-os nas categorias definidas no prompt inicial (Proteína, Leguminosa, Carboidrato, Vegetal, Fruta, Laticínio, Gordura, Condimento, Outro), sem incluir o modo de preparo.
