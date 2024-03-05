# Labb5

## Uppgift 1

### Relationer till klasser
Gör en avvägning kring relationer till externa klasser/interfaces (dvs klasser/interfaces som inte är en del av kodbasen); ta med de relationer som känns viktiga för att klargöra kodbasens design, utelämna de som inte gör det.
- DIP: GameObjects är en abstrakt klass
- ObserverPattern genom JavaSwing
- 

### Avvägningar för konstruktorer och för privata fält och metoder.
Gör liknande avvägningar för konstruktorer och för privata fält och metoder.


## Uppgift 2 

### Analys av kodbasen utifrån de principer vi diskuterar i kursen
Peka ut sådant som bryter mot någon av principerna - sådant finns garanterat, medvetet eller omedvetet gjort - och förklara hur det bryter mot principen i fråga.
Identifiera och förklara (minst) tre olika användningar, eller försök till användningar, av design patterns vi tagit upp i kursen - om sådana existerar i kodbasen.

S - SRP
    Single Responsibility Principle:
        A class should have one, and only one, responsibility, and do it well.

O - OCP
    Open Closed Principle:
        Software models should be open for extension but closed for modification.

L - LSR
    Liskov Substitution Principle:
        A subtype should always be able to used as a substitute for it's supertype.

I - ISP
    Interface Segregation Principle:
        No client should be forced to depend on methods 
it does not use.

D - DIP
    Dependency Inversion Principle:
        Depend on abstraction, not on concrete implementations.