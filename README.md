# Logistic-Coupled-Map-lattice

## Bifurcation Diagram of Logistic Map
![download](https://github.com/user-attachments/assets/44b9349a-db13-44a2-9c65-7b50b2e1898f)

This module has 2 major sections:-
- Logistic Map CML
- Extrapolation part

## <u> Logistic Map CML </u>
This part contains the standard simulation of a Coupled map lattice using the Logistic Map function and equation for lattice. The Logistic Map is a simple non-linear equation having a <b>parameter constant (r)</b> that determines it to be either a periodic phase or a chaotic phase. The CML equation has another parameter <b> coupling strength (epsilon)</b> that controls the interaction of neighbours in determining the next state of lattice cell as written in <u>simulation code function</u> in class <b>logistic_cml</b>.

The idea of dependence of r value onto the phase of the system could be determined by the <b>Bifurcation Diagram</b> that does a great job in visualizing the phase of system w.r.t values of r and giving a fair idea of transition between periodic to chaotic phase w.r.t r_value.

The output of the CML simulation contains four plots:-
- Space-Time irregular plot
![irr](https://github.com/user-attachments/assets/4af49602-898b-4a46-b365-80bfd5fee687)
- Time regular, Space irregular plot
![time reg](https://github.com/user-attachments/assets/31c83cd0-511d-4e57-8e25-f6912d9c81a6)
- Time irregular, Space regular plot
![spave rf](https://github.com/user-attachments/assets/89a1a000-97d4-42e1-a966-f115ebd495b1)
- Space-Time regular plot
![reg](https://github.com/user-attachments/assets/213e8f53-c99d-4dae-8d60-3a2fcf55c42a)


## <u> Extrapolation Part </u>

This part of the module is based on the values of r and epsilon parameters. Unlike in standard CML above, where these parameters were constant, this part tries to simulate CML by applying randomness to these parameter values.

The randomness introduced is of two kinds:-
- Dynamic Randomness
- Lattice Site Randomness

### <u> Dynamic Randomness </u>
Here, the r value and epsilon are varied with iterations, where a particular iteration will only have a constant r and epsilon.

<b> <u>Result </u> </b>:-- The resulting plot obtained showed a time-irregular and space-regular pattern, which failed in the standard CML simulation. This indicates the importance of applying dynamic randomness in parameter values for this pattern.

![dyno](https://github.com/user-attachments/assets/b40b7d1d-e878-4b57-a40a-bf7849048498)

### Lattice Site Randomness
Here, the r value and epsilon vary for each lattice site, i.e., each lattice site has its own r and epsilon parameter.

<b> <u> Result </b> </u> :-- The resulting plot is a irregular space-time plot.

![lattice](https://github.com/user-attachments/assets/ea772a21-6af7-413d-91c4-b8c35da3bdc8)

<u> <b> Note</b> </u>:-- The randomness introduced for the parameter values is probabilistic randomness. The parameter r and epsilon values are divided into two parts via the bridge_num. Please refer to <b> def change_num_prob</b> in the model below for reference.
