# Pseudokod  lösningsförslag

På Liseberg får man bara åka attraktionen Balder ifall man är över 120 cm.

```
START // Här startar vår pseudo code

FUNCTION named checkHeight // En FUNCTION är ett block kod som kan kallas på någon annanstans i koden men koden körs först när den kallas på. I detta exempel på rad 17.
    OUTPUT Hur lång är du?
    INPUT my height in cm // Tar in höjden från användaren i cm
    SET Balder minimum height to 120 cm // Sätter minsta höjden till 120 cm, används för att jämföra mot input

    IF my height is greater then Balder minimun height // Villkor som kollar vår längd är större än minimun längd
        THEN OUTPUT Wheee, Balder!! // Ifall villkoret är sant skriv ut Wheee, Balder!!
    ELSE
        OUTPUT No Balder for you! // Ifall villkoret är falskt skriv ut No Balder for you!
ENDFUNCTION

CALL FUNCTION named checkHeight // Kallar på funktionen checkHeight och kör den koden

END // Här slutar vår pseudo code
```

## Stegen - exempel

Ett tärningspel där användaren ska kasta 1st tärning. Vid första kastet ska målet vara 1. Om 1 ej fås, ska man försöka igen. Hur många kast tar det för att komma upp i en stege, 1,2,3,4,5,6? Kast räknas och den med lägst antal kast vinner.

### Algorithm design

1. Sätt goal till 1
2. Sätt throws till 0
3. Slumpa en siffra mellan 1 till 6
4. Spara den slumpade siffran
5. Jämför den slumpade siffran med goal
6. Öka throws med 1
7. Om den slumpade siffran är lika med goal
    a. Öka goal med 1
    b. Om goal är lika med 7
      a. Skriv ut "Du vann!"
    c. Annars Starta om från steg 1.
8. Annars starta om steg 1.

### Pseudokod

```
START

SET goal to 1
SET throws to 0

FUNCTION named throwDice
    SET dice sides to 6
    CALCULATE a random number between 1 and dice sides
    OUTPUT random number
ENDFUNCTION

FUNCTION named play
    CALL FUNCTION throwDice and save output in diceRoll // Spara värdet från throwDice i diceRoll för att kunna använda senare

    SET throws to plus 1

    IF diceRoll equals goal
        SET goal to plus 1

        IF goal equals 7
            DISPLAY Du vann!
        ELSE
            CALL FUNCTION play
    ELSE
        CALL FUNCTION play
ENDFUNCTION

CALL FUNCTION play

END
```

## Fizzbuzz - exempel

Loopa igenom hundra nummer och om:

* Numret är dividerbart med 3, skriv ut "Fizz"
* Numret är dividerbart med 5, skriv ut "Buzz"
* Numret är dividerbart med 3 och 5, skriv ut "FizzBuzz"

### Pseudokod

```
START

LOOP through 1 to 100
    IF number is dividable by 3 AND number is dividable by 5
        DISPLAY FizzBuzz
    ELSE IF number is dividable by 3
        DISPLAY Fizz
    ELSE IF number is dividable by 5
        DISPLAY Buzz 
ENDLOOP

END
```
