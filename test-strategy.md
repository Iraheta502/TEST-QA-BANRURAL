Correccion #1
Descripcion: Comparar el numero generado con el escrito
Resultado: Boton no realiza accion 
Linea a modificar: 87 y 95
Antes: 87: guessSubmit.addeventListener('click', checkGuess); 95: resetButton.addeventListener('click', resetGame);
Despues: 87: guessSubmit.addEventListener('click', checkGuess); 95: resetButton.addEventListener('click', resetGame);
Resultado Genera la accion

Correccion #2
Descripcion: adivinar un número entre 1 al 100
Resultado: El numero que genera de forma randon 0 al 10 con desimales
Linea a modificar: 44
Antes: let randomNumber = Math.random() * 10;
Despues: let randomNumber = Math.floor(Math.random() * 100) + 1;
Resultado Luego de la modificacion: generara un numero random del 1 al 100 solo enteros 

Correccion #3
Descripcion: El usuario tiene 10 intentos
Resultado: Solo tiene 5 intentos 
Linea a modificar: 46
Antes: const ATTEMPS = 5;
Despues: const ATTEMPS = 10;
Resultado Luego de la modificacion: El usuario puede intentarlo 10 veces

Correccion #4
Descripcion: Mensaje con los colores correspondientes
Resultado: Muestran los colores curzados 
Linea a modificar:  74
Antes: lastResult.style.backgroundColor = 'green' ;
Despues:  lastResult.style.backgroundColor = 'black';
Resultado Luego de la modificacion: El usuario puede intentarlo 10 veces

Correccion #5
Descripcion: Mensaje no corresponde 
Resultado: Muestran los mensajes de ganar y perder de manera erronea 
Linea a modificar:  64 y 69
Resultado Luego de la modificacion: Mensajes correctos

Correccion # 6
Linea a modificar: 57
Antes: let userGuess = guessField.value;
Despues: let userGuess = parseInt(guessField.value);
Resultado:Convierte el string en numero para que la comparacion sea exacta

Correccion # 7
Linea a modificar: 113
Antes: randomNumber = Math.floor(Math.random()) + 1;
Despues: randomNumber = Math.floor(Math.random() * 100) + 1;
Resultado: Cuando se repite el juego el numero randon va de 1 a 100 y no solo a 1

Correcion #8
Se agrega 
if (isNaN(userGuess) || userGuess < 1 || userGuess > 100) {
        alert('Por favor, ingresa un número entero entre 1 y 100.');
        guessField.value = '';
        guessField.focus();
        return; // No se procesa la suposición inválida ni se incrementa el contador
      }
para que no tenga numeros menores ni mayores a 100  y si hay desimales los vuelve un entero 

