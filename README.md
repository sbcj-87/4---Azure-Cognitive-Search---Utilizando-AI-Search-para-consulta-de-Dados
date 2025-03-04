# 4---Azure-Cognitive-Search---Utilizando-AI-Search-para-consulta-de-Dados

# Azure Cognitive Search: Utilizando AI Search para consulta de Dados

Passo a passo do desafio de projeto "Azure Cognitive Search: Utilizando AI Search para consulta de Dados" da DIO.

Links importantes:

- [Explore an Azure AI Search index (UI)](https://aka.ms/ai900-ai-search)
- [Zip com os reviews](https://aka.ms/mslearn-coffee-reviews)

## Passo 1: Criando recursos necessários no Portal do Azure

Primeiro foi preciso criar um recurso do Azure AI Search dentro do Azure AI Services. Em Escalão de preço, utilizei o "Básico".

![Captura de tela 2025-03-03 215145](https://github.com/user-attachments/assets/03ac9482-a6be-421c-9f37-28c0c7afeb44)


Depois foi criado o recurso de Serviços Cognitivos.

![Captura de tela 2025-03-03 215205](https://github.com/user-attachments/assets/8864d66f-05a7-43e8-9e4f-a7fd058a5805)


E após isso, criei uma conta de armazenamento.

![Captura de tela 2025-03-03 215342](https://github.com/user-attachments/assets/690ebf6b-0446-45c7-9097-fb70483a34a6)


Para configurá-la com configurações básicas apenas para este laboratório, precisei liberar o acesso ao container de Blob para anônimos mo Menu lateral na página do recurso > Configurações > Permitir acesso anônimo de Blob.

![Captura de tela 2025-03-03 215533](https://github.com/user-attachments/assets/a266fa32-1e4e-44fd-8203-18cd3be6ed50)


## Importando dados

Para importar os dados, acessei "Armazenamento de dados" > "Contentores" para trazer arquivos. Foi criado um novo container com o nome coffereview e o nível de acesso como "Contentor (Acesso a leitura anônima para contentores e blobs)".

![Captura de tela 2025-03-03 220044](https://github.com/user-attachments/assets/765e0b87-494c-46b9-abba-d4a381b908f7)


Acessei o contentor que eu criei e cliquei no botão "Carregar". Então foi feito o upload dos arquivos de texto disponíveis em [https://aka.ms/mslearn-coffee-reviews](https://aka.ms/mslearn-coffee-reviews).

![Captura de tela 2025-03-03 220928](https://github.com/user-attachments/assets/73969d48-8796-4210-bc8d-0a507ff849c2)


Então tive que acessar o recurso criado para o AI Search e "Importar dados".

Para importar os dados, foi seguido o tópico "Indexar os documentos" deste artigo ([link](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)).

## Testando a pesquisa

Para fazer o teste ser executado, acessei a aba "Explorador de procura" da página do recurso de pesquisa.

Fiz uma pesquisa sobre localidade:

`_search=locations:'Chicago'_

![Captura de tela 2025-03-03 222359](https://github.com/user-attachments/assets/3701b436-f1fd-4266-871c-38bc1e6a34f2)


E outra pesquisa sobre opiniões positivas:

`_search=sentiment:'positive'_

![Captura de tela 2025-03-03 223118](https://github.com/user-attachments/assets/95c31dcf-0422-46b1-ad55-b5e128f73369)




## Excluindo os recursos criados

Para finalizar o projeto, exclui todos os recursos criados para evitar gastos surpresas.
