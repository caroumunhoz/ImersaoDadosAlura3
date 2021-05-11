# ImersaoDadosAlura3

Repositório contendo atividades elaboradas na 3ª Imersão Dados da Alura.


### Problema:
Pensar a construção de drogas farmacêuticas baseado no desafio do [Laboratory innovation science at Havard](https://lish.harvard.edu/) disponibilizado no [kaggle](https://www.kaggle.com/c/lish-moa). No caso dos dados que estamos trabalhando, cada linha representa uma cultura celular. Mas o que é cultura celular? Basicamente, é um grupo de células armazenadas em algum recipiente/ambiente em laboratório para que sejam feitos experimentos. Estes grupos foram submetidos a alguma substância (composto) e foram retiradas seus valores de expressões genéticas, morte de celulas e mecanismo de ativação ativados ou não. Essas medidas foram tiradas com dois tipos de doses diferentes do composto (D1 e D2) em três períodos diferentes: 24, 48 e 72 horas e sem o composto, isto é, o comportamento natural das células em um ambiente artificial criado em laboratório. A partir da análise exploratório dos dados, será indicado pelos instrutores a construção de um modelo de Aprendizado de Máquina que contribua para a descoberta de novas drogas. 

### **Dados**:

_dados_experimentos.zip_:

    Variáveis:
    
    1) Id -> identificador de cada grupo de célula utilizado nos experimentos
    
    2) Tratamento -> Com droga ou com controle. 
      Esta coluna nos diz se a cultura celular havia sido submetida à alguma droga ou estava somente em um ambiente de controle no momento em que foram tiradas as medidas de algumas de suas características. 
      *Ambiente de controle: 
          no contexto científico, diz respeito a isolar os indivíduos nos quais se está realizando um experimento, mas simulando seu ambiente natural de vida, para que haja confiança de que os efeitos observados sejam causados pela droga aplicada e não de outro fator externo.
      
    3) Tempo -> Se tratamento com controle, tempo em que o grupo de células fora isolado no laboratório; se tratamento com droga, tempo desde que a droga foi aplicada até a "anotação" das atuais características das células.
      
    4) Dose -> D1 ou D2. Provavelmente diz respeito à quantidade da droga aplicada: D1 talvez seja uma dose menor que a D2.
      
    5) Droga-> Nome da droga ou composto químico aplicada(o). A maioria são compostos, porém pode haver drogas que estão sendo submetidas a testes novamente. Os nomes foram anonimizados para evitar o viés da análise dos cientistas a partir do conhecimento prévio da substância.
      
    6) G's -> trechos do DNA. Nos traz a informação da reação do gene ao comparar suas medidas com controle e com droga. 
      Neste caso, como existe um processo de proteína gerada por esse elementos, estaríamos interessados em drogas que aumente ou diminui tais medidas do Gene dependendo do problema a ser resolvido.
      
    7) C's -> Tipo celular. Exemplos: células de câncer, células saudáveis etc. Aplicar a substância em vários tipos de célula tem o objetivo de observar os efeitos dos compostos em células com vários tipos de características e garantir que os efeitos se dão pelo composto e não pelo tipo da célula (seres humanos com algum tipo de doença ou não, por exemplo). Os seus valores são o que é chamado de viabilidade celular, isto é, a contagem das células. Neste caso utilizamos pra comparar a quantidade de células sem composto e com aplicação de composto (quantas sobreviveram ou não).
    
_dados_resultados.csv_:

    Variáveis:
        
        1) Id -> identificador de cada grupo de células utilizado nos experimentos
        
        2) Seguido por 210 colunas indicando um mecanismo de ativação e a(o) proteína ou patógeno que esse mecanismo fora ativado. Essas colunas possuem valores de 1 pra indicar se aquele mecanismo de ativação fora ativado ou 0 do contrário no grupo de células indicado pela coluna id. 
