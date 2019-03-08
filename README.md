# sap-cpu

## Version 1

![](Billeder/sap-cpu-v1.png)

Læg to tal sammen:

- Tal i input
- Input Out + A In
- Tal i input
- Input Out + B In
- ALU Out + Output In

## Version 2

![](Billeder/sap-cpu-v2.png)

Læg tal fra RAM sammen

- Tal i RAM på adresse 0 og 1
- 0 i input
- Input Out + MAR In
- Ram Out + A In
- 1 i input
- Input Out + MAR In
- Ram Out + B in
- ALU Out + Output In

## Version 3

### Binære instruktioner

| A Reg In | A Reg Out | B reg In | B reg Out | ALU Out | Input Out | Output In | Mem Addr In | RAM Out |
| -------- | --------- | -------- | --------- | ------- | --------- | --------- | ----------- | ------- |
| AI       | AO        | BI       | BO        | EO      | IO        | OI        | MI          | RO      |
| 1        | 2         | 3        | 4         | 5       | 6         | 7         | 8           | 9       |

Læg til sammen fra RAM

- Tal i RAM på adresse 0 og 1
- 0 i input
- 0000 0101 0 0500 (IO+MI) 
- 1000 0000 1 8080 (AI+RO)