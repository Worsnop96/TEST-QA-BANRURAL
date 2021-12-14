Errores:

1. EL numero random únicamente estaba definido para 10 números, por lo que se procedió a cambiar para 100 números. En la siguiente línea.
   let randomNumber = Math.floor(Math.random() \* 100) + 1;

2. El número de intentos estaba definido únicamente solo a 5 intentos, la solución de esto es cambiar la definición a 10 a la siguiente variable
   const ATTEMPS = 10;

3. El campo en donde se ingresan los datos numéricos admite letras y decimales. La solución para ello es definir el input como un campo de tipo number
   <input type="number" id="guessField" class="guessField" />

Y adicional a esto agregando la siguiente comprobación.

if (Number.isInteger(userGuess))

4. Los casos en las condicionales entre el numero ingresado y el numero random deben ser arreglados tanto en el mensaje enviado como en el color en el que se presenta el mensaje
   if (userGuess === randomNumber) {
   lastResult.textContent = "Felicitaciones! adivinaste el número!";
   lastResult.style.backgroundColor = "green";
   ….

5. el mensaje que se envia al momento de alcanzar el limite de intentos estaba equivocado por lo que se corrige y se le asigna el color correspondiente.
   else if (guessCount === ATTEMPS) {
   lastResult.textContent = "!!!Perdistes!!!";
   lowOrHi.textContent = "";
   setGameOver();
