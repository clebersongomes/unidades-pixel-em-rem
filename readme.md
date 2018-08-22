# Pixels, RM ou REM?



### Pixels

Responsável por definir altura, largura, tamanhos de texto e etc... Acredito que seja o método mais utilizado mesmo sendo antigo.

	body {
		font-family: Arial,Helvetica Neue,Helvetica,sans-serif;
		font-size: 10px;
	}

### EM

Pensando em um layout que se adapta em diversos tamanhos de telas, recomendo utilizar essa medida, é importante entender como calcular.

    <body>
	    <p>Exemplo</p>
    </body>

    <style>
	    .body{
		    font-family: Arial, Heveltica Neue, Helvetica, sans-serif;
		    font-size: 12px;
	    }
	    p{
		    font-size: 14px;
	    }
    </style>
  
Nosso paragrafo tem um tamanho de 14px que é o elemento que queremos modificar o body nesse casso é o pai do nosso elemento. Para descobrir qual o valor do EM, precisamos fazer uma conta simples 14/12 = 1.16.

    <style>
	    p{
		    font-size: 1.16em;
	    }
    </style>

Caso nosso elemento "p" esteja em cima de algum outro elemento pai, o pai dele deve ter um valor definido no font-size e o calculo tem que ser realizdo por ele.

### REM

Muito parecido com o EM, mas o que define esse "R" é que o pai sempre vai ser o body independente do pai do elemento.

Obs.: Esse tipo de calculo só é suportado por alguns navegadores Firefox 3.6+, Chrome, Safari 5, e IE9.

    <body>
	    <div>
		    <p>Exemplo</p>
		</div>
    </body>

    <style>
	    .body{
		    font-family: Arial, Heveltica Neue, Helvetica, sans-serif;
		    font-size: 12px;
	    }
	    p{
		    font-size: 1.16px;
	    }
    </style>