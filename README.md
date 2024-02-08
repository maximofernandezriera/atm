# atm
https://www.codewars.com/kata/5635e7cb49adc7b54500001c


# Kata ATM

El kata implica escribir una función para un cajero automático para determinar el número mínimo de billetes necesarios para realizar un retiro de cierta cantidad (n dólares), donde 1 <= n <= 1500. El cajero dispensa billetes de valores nominales de 10, 20, 50, 100, 200 y 500 dólares, asumiendo un suministro ilimitado. La función deberá devolver el número mínimo de billetes o -1 si es imposible dispensar la cantidad exacta.

## Pasos a seguir

1. Definir la clase `ATMSolution` con un método `main` para pruebas.
2. Dentro de la clase, definir el método `calculateMinimalNumberOfBanknotes(int n)` que implementa nuestra solución.
3. Codificar la lógica para determinar el número mínimo de billetes o devolver -1 si es imposible.


## PseudoCódigo

```vb

    Function CalculateMinimalNumberOfBanknotes (Integer) As Integer
        If n Mod 10 <> 0 Then
            Return -1 ' Si n no es múltiplo de 10, retorna -1
        End If

        billetes Integer = {500, 200, 100, 50, 20, 10}
        contador  Integer = 0

        For Each billete As Integer In billetes
            While n >= billete
                n -= billete
                contador += 1
            End While
        Next

        Return contador
    End Function

```

