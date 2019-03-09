# sap-cpu

## Version 1

Dette er den manuelle version af en CPU. Den består af 

- Et 8 bit A register
- Et 8 bit B register
- En 8 bit ALU som udelukkende kan lægge bit sammen fra A og B (ingen hensyntagen til mente)
- En 8 bit databus
- Et 8 bit output register
- Manual input til databus (til test)
- En clock

![](Billeder/sap-cpu-v1.png)

### Få et tal fra input og læg det sammen med sig selv

Samtlige kontrollinjer skal påvirkes manuelt (brug ctrl + T til at få klokken til at slå)

- Tal i input
- Input Out (IO) + A In (AI)
- Input Out (IO) + B In (BI)
- ALU Out (EO) + Output In (OI)

## Version 2

![](Billeder/sap-cpu-v2.png)

Find et tal i RAM (adresse 0) og læg det sammen med sig selv

- Tal i RAM på adresse 0 
- 0 i input (0 ved reset)
- Input Out + MAR In
- Ram Out + A In
- A Out + B in
- ALU Out + Output In

## Version 3

### Binære instruktioner

| A Reg In | A Reg Out | B reg In | B reg Out | ALU Out | Input Out | Output In | Mem Addr In | RAM Out |
| -------- | --------- | -------- | --------- | ------- | --------- | --------- | ----------- | ------- |
| AI       | AO        | BI       | BO        | EO      | IO        | OI        | MI          | RO      |
| 1        | 2         | 3        | 4         | 5       | 6         | 7         | 8           | 9       |

Find et tal i RAM (adresse 0) og læg det sammen med sig selv

- Placer tal i RAM på adresse 0 
- (0 i input) - ikke nødvendig fordi input = 0 ved reset
- 1010 0111 0 = A700 RESET ALT
- 0000 0101 0 = 0500 (IO+MI) 
- 1000 0000 1 = 8080 (AI+RO)
- 0110 0000 0 = 6000 (AO+BI)
- 0000 1010 0 = 0A00 (EO+OI)