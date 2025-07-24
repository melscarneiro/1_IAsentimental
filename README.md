  

# Análise de Sentimentos com Language Studio no Azure AI

*Projeto - Laboratório 03 - Bootcamp Análise de dados Randstart*


 
# Introdução



O Processamento de Linguagem Natural (PLN) é uma área da Inteligência Artificial (IA) voltada para a interpretação da linguagem humana, seja escrita ou falada. Entre suas principais aplicações, destaca-se a análise de sentimentos, que identifica automaticamente emoções e opiniões em textos, como avaliações de produtos e feedbacks de clientes.

Para que a IA compreenda o texto, ocorre um processo chamado tokenização, que divide a frase em partes menores (tokens) e, a partir daí, aplica técnicas de PLN para interpretar o contexto e a relação entre as palavras.

Essa análise permite maior eficiência na interpretação de grandes volumes de dados e oferece confiança nas informações, sendo útil para empresas que desejam entender a percepção dos consumidores sobre seus produtos.

  

# Exemplo Prático


Realizei a extração de avaliações reais de compras realizadas na Amazon sobre o modelo de fone de ouvido JBL Tune 770NC.

Após o upload do arquivo, o **Azure Language Studio** realiza o processamento das frases, dividindo-as em sentenças (**assessment**) e classificando cada uma como positiva, neutra ou negativa, atribuindo pontuações de confiança (de 0 a 1).

*As preposições adversativas (como “mas” e “porém”) também são consideradas como mudança de opinião dentro da mesma sentença.*


## :wrench: Ferramentas utilizadas

- Azure Language Studio – Analyze Sentiment

- Extensão Data Minders (Google Chrome)


# Como o Azure AI Classifica os Sentimentos

  

Segundo a documentação do Azure AI – Analyze Sentiment, a classificação segue as seguintes regras:

|Tipo de frases   |Resultado  |
|----------------------------|----------------------------|
|Todas as frases neutras     |→ sentimento geral neutro.  |
|Frases positivas + neutras  |→ sentimento geral positivo.|
|Frases negativas + neutras  |→ sentimento geral negativo.|
|Frases positivas + negativas|→ sentimento geral misto.   |

Exemplo, com a análise abaixo:
1. Avaliação 100% positiva
**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe58nwIh43QGJRaC61QOB8twF0d7QIJFU0Bsa-sLtDX9BrJpbPtjyNLzh5GFH5FJVTvZpJ29UKPqs_k0wT7xd0dIa6k3Hs4Rtld-s6EHr-jHC9Zrvphrzd2CJ1dpv8rlVGTgp1ajw?key=LaiN8D1EoBxk780zGWZF8w)**

2. Avaliação Positiva e Negativa
**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeaY29M2NdrLtxTxPtKB3xkqixQI3VjbHaJelpRMRVAanl4xCYYkF8FYyHAF0lHvvG2QgYIJGd-lSuuwKkS2Rp6HhH4Z9jhxMwVXZe9TYRvlJTDU4SHOOGP3hR_h3z4sJb8liHIUQ?key=LaiN8D1EoBxk780zGWZF8w)**

## Exemplo de Interpretação

Em algumas situações, frases curtas ou ambíguas podem causar interpretação errada pela IA.  
Por exemplo, a palavra “Alto” foi classificada como negativa (55%), enquanto para o usuário poderia ser algo positivo (som alto de qualidade).
**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-F54-3BcOE_DnIF4pZrAcv6fCZdACpRYzgaEwj6Mf2oetCYKCHfqw5E5sGmEdhRCZ9tVRLsvqMrdM0ziXwjHBplbvCb9JSv_Y7LFLsMTF6_9LhSsWhv0FzfR2OkCUkiPCH1jPmA?key=LaiN8D1EoBxk780zGWZF8w)**

Essa análise se torna mais assertiva ao observarmos que para frases curtas a atribuição “**se as classificações de frases incluírem tanto termos positivos quanto negativos, o sentimento geral será considerado misto.**” o modelo de processamento pode interpretar que a ambiguidade faz com que temos uma incerteza sobre a avaliação.

No caso de frases curtas, ambíguas ou com pouco contexto, mesmo que a intenção do usuário seja positiva, o modelo de processamento pode interpretar de forma diferente. Nessa situação, uma pontuação de **62% de neutralidade indica que não há um sentimento predominante detectado**.*

## **Desafios atuais na análise de sentimentos**

Um dos principais desafios está na interpretação da linguagem coloquial e das ambiguidades.

Por exemplo, ao identificar uma palavra com conotação negativa, o modelo pode atribuir apenas 17% de negatividade, ignorando o contexto real, que na verdade expressa um elogio ao produto.

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdxhgY4oC4zZXB3jiNWDmsNJFpHRevbum8xpxZr-36BGnlv7xUF4pZ8QXAnqOsLk1LvKFYV6iP8DEcVXalQLPRszv66-N4zxQFSMYPE-HzNAH-s7ISNXgZsLGXsfCGX2eCZv_i_gw?key=LaiN8D1EoBxk780zGWZF8w)**
**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdEtXDGtcBfxhGGJNY2E-MqkiHkGVb9QgNHwbkgh_rZlSU8lwG5y9pG10uyfN5WdYxtGVnRIUQo3u4e0j3Q-Y6ieinJHNlNkhXQYPcI2xniMhrU57EbnrU_In5xQxfAedHECaJygA?key=LaiN8D1EoBxk780zGWZF8w)**

Através dessa pequena análise, identificamos que o processamento de dados efetuado pela análise de sentimento no Azure AI permite automatizar a interpretação de comentários de clientes, oferecendo insights rápidos e relevantes para as organizações.

Como conclusão entendemos que, a análise humana qualitativa continua sendo essencial para interpretar ambiguidades e nuances da linguagem, assim como possibilitar com que esse processo seja desenvolvido e utilizado com muita eficiência. 

*Contribua com o projeto e com mais informações! Estou aprendendo. (:*

:punch:
