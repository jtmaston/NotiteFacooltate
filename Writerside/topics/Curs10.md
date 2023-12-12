# Curs11

- DMU = digital mock-up
- Definim cuple
  - Revolute = de rotatie
  - Prismatic = de translatie
  - Cylindrical = rotatie + translatie (dar independente)
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
3. Fix part (ancora)
   - ![ss2.png](ss2.png)
4. Simulation, automatic insert
   - ![ss3.png](ss3.png)
5. Compile simulation
   - ![ss4.png](ss4.png)
6. Alegem replay (catia) sau animation file (universal)

## Parametrizare!
1. Apasam F(x)
    ![image_1.png](image_1.png)
2. New parameter of type -> atenție, punem explicit unitatea de măsură (mm) (length!)
    ![image_2.png](image_2.png)
3. Pentru editat cota: BdM, [obiect].object, edit formula (atentie, click pe cota, nu pe linie)
    ![image_3.png](image_3.png)
4. Daca nu ai setat explicit unitatea de masura, urla la tine!
    ![image_4.png](image_4.png)
5. Dupa modificare
    ![image_5.png](image_5.png)

## Prismatic
1. Faci un joint nou
   - Selectezi liniile care tre sa fie an contact
   - Selectezi planele care sunt an contact
   - Comanda este in lungime
2. Fix parts
3. Profit!

## Exemplu folosind robotu'
![image.png](image.png)

Pe rand, joint-uri revolute in care selectam axele cilindrelor, iar apoi suprafetele de asezare. Daca este nevoie, putem
pune un offset, ca sa simulam jocurile.

Mentiuni: daca e de facut dmu, se cauta roboti care au piesele puse separat, (joint1.step, join2.step) etc, DAR! daca
gasim un step cu toate chestiile intr-una, deschidem step-ul, si salvam individual fiecare body din ansamblu.

Pentru constrangeri / elemente de simulare, se pot lua doar din acelasi subansamblu!


