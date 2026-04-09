# Relatório - Coelinhos da Páscoa

<!-- > [!CAUTION]
> - Lembre-se que você <ins>**não pode utilizar ferramentas de IA para
>   escrever este relatório**</ins> -->

## Dados do aluno

- **Cartão UFRGS**: 591004
- **Nome**: Caetano Meneghetti

## Passos que eu segui para resolver o problema especificado (em formato de *"prompt"*)

<!-- > [!IMPORTANT]
> - Coloque aqui todas as informações necessárias para que alguém
>   (pessoa ou ferramenta de IA) possa reproduzir os seus passos para
>   solucionar o problema
> - Escreva em formato imperativo, como se fosse um *prompt* com as
>   instruções a serem seguidas na solução do problema
> - Seja objetivo e conciso: quanto *menos palavras* você utilizar,
>   melhor
> - Seja técnico e use terminologia adequada: assuma que quem irá ler
>   os seus passos possui conhecimento de Ciência da Computação e
>   Computação Gráfica
> - Caso você queira incluir informações "longas" (como algum *prompt*
>   grande usado com alguma ferramenta de IA), crie arquivos à parte e
>   adicione links no texto (por exemplo, crie o arquivo `PROMPTS.md`
>   e adicione um link markdown `[os prompts detalhados estão
>   aqui](PROMPTS.md)`)
> - Novamente, lembre-se que você *não pode utilizar ferramentas
>   de IA para escrever este relatório* -->

Crie um script em python que recebe o arquivo *data/sphere.obj* e retorna um arquivo *data/egg.obj*. O arquivo de entrada é a definição padrão Wavefront OBJ com vértices, normais e faces de uma esfera. Deixe essa esfera oval, mantendo os valores normalizados entre -1 e 1.

Partindo do arquivo `main.cc`, desenhe 16 coelhos (*bunny.obj*), cada um com 2 ovos (*egg.obj*) como objetos filhos. Os coelhos devem estar dispostos em um círculo em torno da origem, cujo raio deve ser tal que os coelhos não fiquem tão próximos uns dos outros (talvez um raio igual a 8.0). Ou seja, cada um dos 16 coelhos deve estar em um ângulo diferente dentro do círculo. Esses coelhos devem estar se mexendo ao longo da circunferência continuamente e também se movimentando verticalmente de forma senoide (o resultado dessas duas translações deve ser como um movimento senoidal em torno da circunferência). Os ovos devem seguir o coelho sempre. Um a cada quatro coelhos deve estar girando para frente (tangente à circunferência do círculo que está se mexendo), mas os ovos ligados à ele não devem fazer esse giro, então uma opção pode ser simplesmente usar uma matriz que anula esse *spin*. Use tanto o valor de tempo do glfwGetTime() quanto o ângulo (i * (2.0f * M_PI / 16)) para definir as transformações.

## Principais dificuldades encontradas durante o desenvolvimento (formato livre)

Nenhuma grande dificuldade. Foi apenas um processo iterativo de encontrar os valores que deixavam o resultado cada vez mais parecido com o vídeo.

## Você acha que conseguiu resolver o problema de forma adequada?

Acredito que sim. Colocando o vídeo do resultado esperado e a execução do meu programa, não consegui detectar nenhuma diferença significativa.

<!-- ## Se você quiser compartilhar mais alguma coisa, coloque aqui:

## Se você possui alguma sugestão para o professor sobre esta atividade, coloque aqui:
