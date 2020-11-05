# Entrega 5: Replicar casos 2-D para verificar

1. Descripción de como hay que cambiar las condiciones de borde, en el código.
   
Para cambiar las condiciones de borde se debe considerar que los lados se representan de la siguiente forma:

  Borde izquierdo: u_k [0 , :]

  Borde derecho: u_k [-1 , :]

  Borde superior: u_k [: , -1]

  Borde inferior: u_k [: , 0]

  Entonces, para condiciones de borde con valores constantes simplemente se iguala la variable que corresponde al borde a la temperatura que se indica para cada caso, por ejemplo,
  si la condicion inicial para el borde izquierdo es de 20° grados, entonces se define de la siguiente forma:

  u_k [0 , :] = 20.

  Para los casos en que la condición de borde corresponde a un gradiente se considera la siguiente expresion:

  (f(x+h) - f(x) ) / dx = gradiente

  Lo que representado en el codigo se escribe de la siguiente forma:

  (borde x - borde x en paso de tiempo anterior) dividido en dx = gradiente

  Asi, si el borde derecho tiene como condicion inicial un gradiente de 20°, como codigo esto se ve como:

  (u_k [-1 , :] - u_k [-2 , :])/dx = -20.

  Finalmente se despeja el borde derecho que se definió en un principio:

  u_k [-1 , :] = 20. * dx + u_k [-2 , :]
  
  Asi, se pudo obtener los resultados que se esperaban.
  
  Cabe destacar que los resulatdos que se presentaron como comparacion se encontraban en condiciones de a/2 y de 0b, 1/4b, 2/4b, 3/4b. Asi, se obtienen los siguientes graficos:
  
   - Caso 1

Se obtiene el mismo grafico esperado, las condiciones de borde eran las señaladas


![EvolucionT_caso_1](https://user-images.githubusercontent.com/69157203/98262781-c3f90680-1f64-11eb-826a-d6e6a788d1a2.png)
  
  - Caso 2

Las condiciones de borde señaladas no eran las mismas que las señalas, ya que el gradiente de temperatura del borde derecho no es 0°C, sino -10°C. Asi se corrige y se obtiene el siguiente grafco, igual al entregado.

![EvolucionT_caso_2](https://user-images.githubusercontent.com/69157203/98262783-c4919d00-1f64-11eb-81af-37f2a8d939b2.png)

- Caso 3

Se obtiene el mismo grafico esperado, las condiciones de borde eran las señaladas

![EvolucionT_caso_3](https://user-images.githubusercontent.com/69157203/98262785-c52a3380-1f64-11eb-971f-2163e6548e15.png)

 - Caso 4

Se obtiene el mismo grafico esperado, las condiciones de borde eran las señaladas
 
 ![EvolucionT_caso_4](https://user-images.githubusercontent.com/69157203/98262786-c52a3380-1f64-11eb-92b3-9714d27db1c9.png)
 
  - Caso 5

Se obtiene el mismo grafico esperado, las condiciones de borde eran las señaladas
 
 ![EvolucionT_caso_5](https://user-images.githubusercontent.com/69157203/98262787-c5c2ca00-1f64-11eb-9785-57af14667a2b.png)
 
   - Caso 6

Se obtiene el mismo grafico esperado, las condiciones de borde eran las señaladas

![EvolucionT_caso_6](https://user-images.githubusercontent.com/69157203/98262772-c22f4300-1f64-11eb-9fb9-d9cf1e0bf7da.png)

    - Caso 7

Las condiciones de borde señaladas no eran las mismas que las señalas, ya que al entregar las condiciones dadas, no se reproduce de igual manera, resultado el siguiente grafico:

![EvolucionT_caso_7_enunciado](https://user-images.githubusercontent.com/69157203/98262778-c3f90680-1f64-11eb-936d-4e4b26288415.png)

 Mirando la animacion GIF, se obsrva que el comportamiento es similar al esperado, pero una condicion de borde inferior, no es la adecuada.
 
 ![ev_caso_7_enunciado](https://user-images.githubusercontent.com/69157203/98263794-f9522400-1f65-11eb-8623-4eaecccc8c35.gif)
 
 Asi, se reconoce que la condicon de borde inferior, no esta definida por el gradiente, sino por la temperatura del lado inferior igual a 20°C. Asi, se obtiene el siguiente grafico, similar al anterior.
 
 ![EvolucionT_caso_7](https://user-images.githubusercontent.com/69157203/98262775-c3607000-1f64-11eb-8bd7-aee7058857f2.png)
 
2. En un mismo gráfico la evolución de la temperatura en el tiempo en los puntos 

La evolucion de temperatura de los puntos señalados esta descrita por los siguientes graficos:

- Caso 1


![EvolucionT_caso_1_puntos](https://user-images.githubusercontent.com/69157203/98265013-4be01000-1f67-11eb-9c40-5124c34c940f.png)

- Caso 2

![EvolucionT_caso_2_puntos](https://user-images.githubusercontent.com/69157203/98265016-4c78a680-1f67-11eb-9361-0d0f5c8290eb.png)

- Caso 3

![EvolucionT_caso_3_puntos](https://user-images.githubusercontent.com/69157203/98264998-48e51f80-1f67-11eb-8315-a7c265434ef0.png)

- Caso 4

![EvolucionT_caso_4_puntos](https://user-images.githubusercontent.com/69157203/98265003-4a164c80-1f67-11eb-96f7-9d248696a798.png)

- Caso 5

![EvolucionT_caso_5_puntos](https://user-images.githubusercontent.com/69157203/98265007-4aaee300-1f67-11eb-8caa-59dd736a5183.png)

- Caso 6

![EvolucionT_caso_6_puntos](https://user-images.githubusercontent.com/69157203/98265008-4aaee300-1f67-11eb-902f-c1530a501936.png)

- Caso 7

![EvolucionT_caso_7_puntos](https://user-images.githubusercontent.com/69157203/98265012-4b477980-1f67-11eb-8ea7-fa1d0724ccee.png)


3. Imágenes fijas para la distribución de temperatura en los tiempos 0h, 2h, 6h, 12h, 24h y un gif animado con toda la evolución de temperatura. 

- Caso 1

![frame_0000](https://user-images.githubusercontent.com/69157203/98265391-cc067580-1f67-11eb-9ac3-d438e33c929a.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98265396-cd37a280-1f67-11eb-915b-2d566226799a.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98265398-cd37a280-1f67-11eb-9fbf-e5c274a1126c.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98265400-cdd03900-1f67-11eb-9416-68047fbb2a6d.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98265402-cdd03900-1f67-11eb-83ab-328a1e395a81.png)

![ev_caso_1](https://user-images.githubusercontent.com/69157203/98267013-ad08e300-1f69-11eb-8f0e-c06b09e7d075.gif)

- Caso 2

![frame_0000](https://user-images.githubusercontent.com/69157203/98265474-e4769000-1f67-11eb-9349-25a54e8fe33a.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98265480-e50f2680-1f67-11eb-90dd-f72c940241df.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98265483-e50f2680-1f67-11eb-8a16-47a7ef103f10.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98265468-e3456300-1f67-11eb-8cc6-ddbcad26de91.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98265470-e3ddf980-1f67-11eb-8d00-9495154a16de.png)

![ev_caso_2](https://user-images.githubusercontent.com/69157203/98267020-aed2a680-1f69-11eb-90bc-af28e4ceccf5.gif)

- Caso 3


![frame_0000](https://user-images.githubusercontent.com/69157203/98265575-007a3180-1f68-11eb-928c-1cb51633bdf9.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98265578-01ab5e80-1f68-11eb-96c2-f7d7666c84b2.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98265581-01ab5e80-1f68-11eb-88d6-f56f76943018.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98265585-0243f500-1f68-11eb-91fe-2689c217cbe3.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98265586-02dc8b80-1f68-11eb-931c-5eefb5f86cdc.png)

![ev_caso_3](https://user-images.githubusercontent.com/69157203/98267035-b2662d80-1f69-11eb-919f-67885bce6638.gif)

- Caso 4

![frame_0000](https://user-images.githubusercontent.com/69157203/98265685-256ea480-1f68-11eb-9eb2-78667ab98085.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98265687-269fd180-1f68-11eb-83ea-2d4e880f1a69.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98265688-27386800-1f68-11eb-8e2a-e6f1e3ff7fcf.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98265689-27386800-1f68-11eb-87af-baa6ce7e7bd8.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98265693-27d0fe80-1f68-11eb-9853-30f1663e83db.png)

![ev_caso_4](https://user-images.githubusercontent.com/69157203/98267043-b4c88780-1f69-11eb-8c6c-49842495dfe5.gif)

- Caso 5

![frame_0000](https://user-images.githubusercontent.com/69157203/98265731-34555700-1f68-11eb-974b-67b25e4166df.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98265732-35868400-1f68-11eb-98f1-2b2ed7c2bcdf.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98265733-35868400-1f68-11eb-9c56-75a8d9b791b7.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98265734-361f1a80-1f68-11eb-93ce-2254ffccdd0d.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98265735-36b7b100-1f68-11eb-9ac0-aabc6ded93ce.png)



![ev_caso_5](https://user-images.githubusercontent.com/69157203/98267051-b5f9b480-1f69-11eb-9401-ed7dd73c28db.gif)

- Caso 6

![frame_0000](https://user-images.githubusercontent.com/69157203/98265788-446d3680-1f68-11eb-8051-23887beb31c8.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98265790-459e6380-1f68-11eb-8dde-6c2038b0d181.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98265793-459e6380-1f68-11eb-8e5c-157ea217bbf2.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98265796-4636fa00-1f68-11eb-9803-e3407eedea1f.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98265801-46cf9080-1f68-11eb-9108-94200661ed00.png)

![ev_caso_6](https://user-images.githubusercontent.com/69157203/98267059-b85c0e80-1f69-11eb-97f1-b160a2008f49.gif)

- Caso 7

![frame_0000](https://user-images.githubusercontent.com/69157203/98266873-8fd41480-1f69-11eb-81fd-1525ca3378ea.png)
![frame_0002](https://user-images.githubusercontent.com/69157203/98266877-906cab00-1f69-11eb-98ba-1f088b52b7aa.png)
![frame_0006](https://user-images.githubusercontent.com/69157203/98266881-91054180-1f69-11eb-8c23-59aa7b658635.png)
![frame_0012](https://user-images.githubusercontent.com/69157203/98266885-91054180-1f69-11eb-928d-3261ec3c1fe5.png)
![frame_0024](https://user-images.githubusercontent.com/69157203/98266886-919dd800-1f69-11eb-8e5f-a0e0dd1e8650.png)

![ev_caso_7](https://user-images.githubusercontent.com/69157203/98266990-a7ab9880-1f69-11eb-8480-3bad669c1d49.gif)

4. Explique ¿como cambia el código para el caso 3-D? ¿Como se imponen las condiciones de borde?



  
