# Curs10

- DMU = digital mock-up
- Definim cuple
  - Revolute = de rotatie
  - Prismatic = de translatie
  - Cylindrical
  - Screw = rototranslatie

&nbsp

1. Aducem toate piesele in DMU
2. Definesc cuplele
   - Commands
   - Fix parts
3. Simularea
4. Compile simulation
5. Replay (înregistrarea comenzilor)

### !!! MECHANISM CAN BE SIMULATED !!! -> fără asta nu se poate simula

## Aplicație:
1. Create joint : IMPORTANT! SE SELECTEAZĂ PART-ul CARE SE MIȘCĂ!
   - ![ss1](ss1.png)
2. Mechanism -> new mechanism -> selectam daca angle driven sau length driven
3. Fix part (anchor)
   - ![ss2.png](ss2.png)
4. Simulation, automatic insert
   - ![ss3.png](ss3.png)
5. Compile simulation
   - ![ss4.png](ss4.png)
6. Alegem replay (catia) sau animation file (universal)

## Parametrizare!
1. Apasam F(x)
2. New parameter of type -> atenție, punem explicit unitatea de măsură (mm)
3. Pentru editat cota: BdM, [obiect].object, edit formula (atentie, click pe cota, nu pe linie)

## Prismatic
1. Faci un joint nou
   - Selectezi liniile care tre sa fie an contact
   - Selectezi planele care sunt an contact
   - Comanda este in lungime
2. Fix parts
3. Profit!