## 29/09
#Circuit Breaker
resolve o problema de quando um sistema chama outro, mas não se pode garantir que o outro está no ar;
proteger comunicação entre sistemas;
é como um dijuntor, fechado = tudo bem, aberto = falha;
tem que ligar o "dijuntor" de novo, e ficar de olho se vai dar problema, closed, open, half-open;
-half-open: tenta conectar e verifica se vai funcionar, se der certo ele conta, se der errado volta pro open, ao atingir a contagem predefinida ele volta ao estado de fechado;

