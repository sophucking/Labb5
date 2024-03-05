# Labb5

## Uppgift 1

### Relationer till klasser
Gör en avvägning kring relationer till externa klasser/interfaces (dvs klasser/interfaces som inte är en del av kodbasen); ta med de relationer som känns viktiga för att klargöra kodbasens design, utelämna de som inte gör det.
- DIP: GameObjects är en abstrakt klass
- ObserverPattern genom JavaSwing/awt
- 

### Avvägningar för konstruktorer och för privata fält och metoder.
Gör liknande avvägningar för konstruktorer och för privata fält och metoder.


## Uppgift 2+3 

### Analys av kodbasen utifrån de principer vi diskuterar i kursen
#### Peka ut sådant som bryter mot någon av principerna - sådant finns garanterat, medvetet eller omedvetet gjort - och förklara hur det bryter mot principen i fråga och föreslå minst en generell förbättring av kodbasen, med hänvisning till de designprinciper vi tagit upp i kursen. 
S - SRP
    Single Responsibility Principle:
        A class should have one, and only one, responsibility, and do it well.
- Bullet.java handles:
-- a bullet, position, size, damage
-- how it updates each tick
--- if should be removed from array of GameObjects
-- which monster is it's target
-- how it's represented on the screen
-- what panel it's stored in and drawn on

- Map.java handles: 
-- the map, reading the textfile and creating a block-matrix from it, identifying tower positions, the start/end points, what path the monsters need to take. 
--- also handles how the map is painted
-- placing towers on the map (where allowed)

O - OCP
    Open Closed Principle:
        Software models should be open for extension but closed for modification.

L - LSR
    Liskov Substitution Principle:
        A subtype should always be able to used as a substitute for it's supertype.

I - ISP
    Interface Segregation Principle:
        No client should be forced to depend on methods it does not use.

\- Every method in every class is public, there are no interfaces, everything is public everything can accesed by everything. 

D - DIP
    Dependency Inversion Principle:
        Depend on abstraction, not on concrete implementations.



##### Monster
- SRP/MVC: view should not be handled inside model: paint method should not exist inside monster class. 
- OCP: Not extensible, creating new types of monster/enemy would need to  
-- almost closed for modification, the setHealth method hould have been a takeDamage method, also an observer pattern could be used to inform listeners that a moster has died.


#### Identifiera och förklara (minst) tre olika användningar, eller försök till användningar, av design patterns vi tagit upp i kursen - om sådana existerar i kodbasen.
\+ GameObject has an abstract update method and is a supertype to Bullet, Monster and Tower. GamePanel uses a GameObject array to loop through and call the update method in each of them. 
#### Föreslå minst en rimlig användning av ett designmönster, som kodbasen inte redan använder (eller använder felaktigt), och beskriv hur denna förändring skulle påverka kodbasens design, positivt eller negativt.

Observer pattern is used in GameFrame and GamePanel to check for mouse events and timer ticks. However the implementation is lackluster. 



