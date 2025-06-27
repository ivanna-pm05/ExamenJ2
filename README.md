# ExamenJ2
# 🧪 Examen Tipo A 

## 🔗 Sección 1: JOINs (5 problemas)

### 1.

**Enunciado:** Mostrar los empleados junto al país donde laboran.  

```sql
SELECT e.nombre, p.nombre
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
JOIN municipio m ON s.municipioid = m.id
JOIN departamento dp ON m.depid = dp.id
JOIN pais p ON dp.paisid = p.id;
```

```
+-------------------+----------+
| empleado          | pais     |
+-------------------+----------+
| Sofía Pérez       | Colombia |
| Pedro Gómez       | Colombia |
| Carlos Gómez      | Colombia |
| Ana Gómez         | Colombia |
| Sofía Rodríguez   | Colombia |
| Sofía Rodríguez   | Colombia |
| Pedro Gómez       | Colombia |
| Laura Gómez       | Colombia |
| Carlos Pérez      | Colombia |
| Carlos Pérez      | Colombia |
| Carlos Torres     | Colombia |
| Sofía Rodríguez   | Colombia |
| Sofía Torres      | Colombia |
| Sofía Pérez       | Colombia |
| Ana Gómez         | Colombia |
| Pedro Rodríguez   | Colombia |
| Pedro Torres      | Colombia |
| Luis Rodríguez    | Colombia |
| Luis Pérez        | Colombia |
| Sofía Gómez       | Colombia |
| Carlos Pérez      | Colombia |
| Ana Torres        | Colombia |
| Ana Rodríguez     | Colombia |
| Luis Rodríguez    | Colombia |
| Luis Torres       | Colombia |
| Sofía Gómez       | Colombia |
| Laura Rodríguez   | Colombia |
| Ana Gómez         | Colombia |
| Ana Torres        | Colombia |
| Luis Pérez        | Colombia |
| Laura Rodríguez   | Colombia |
| Luis Torres       | Colombia |
| Luis Rodríguez    | Colombia |
| Ana Pérez         | Colombia |
| Ana Gómez         | Colombia |
| Sofía Torres      | Colombia |
| Sofía Gómez       | Colombia |
| Luis Rodríguez    | Colombia |
| Laura Pérez       | Colombia |
| Sofía Gómez       | Colombia |
| Carlos Torres     | Colombia |
| Laura Gómez       | Colombia |
| Luis Gómez        | Colombia |
| Sofía Pérez       | Colombia |
| Sofía Rodríguez   | Colombia |
| Pedro Gómez       | Colombia |
| Ana Pérez         | Colombia |
| Ana Pérez         | Colombia |
| Sofía Torres      | Colombia |
| Ana Rodríguez     | Colombia |
| Sofía Rodríguez   | Colombia |
| Luis Rodríguez    | Colombia |
| Luis Gómez        | Colombia |
| Ana Torres        | Colombia |
| Pedro Rodríguez   | Colombia |
| Luis Pérez        | Colombia |
| Ana Rodríguez     | Colombia |
| Laura Pérez       | Colombia |
| Pedro Rodríguez   | Colombia |
| Ana Gómez         | Colombia |
| Sofía Torres      | Colombia |
| Ana Gómez         | Colombia |
| Sofía Torres      | Colombia |
| Luis Pérez        | Colombia |
| Luis Rodríguez    | Colombia |
| Luis Gómez        | Colombia |
| Laura Torres      | Colombia |
| Laura Torres      | Colombia |
| Carlos Rodríguez  | Colombia |
| Luis Rodríguez    | Colombia |
| Luis Pérez        | Colombia |
| Laura Gómez       | Colombia |
| Carlos Rodríguez  | Colombia |
| Sofía Torres      | Colombia |
| Laura Pérez       | Colombia |
| Laura Gómez       | Colombia |
| Sofía Rodríguez   | Colombia |
| Carlos Torres     | Colombia |
| Luis Torres       | Colombia |
| Pedro Rodríguez   | Colombia |
| Sofía Gómez       | Colombia |
| Luis Gómez        | Colombia |
| Sofía Rodríguez   | Colombia |
| Carlos Rodríguez  | Colombia |
| Sofía Gómez       | Colombia |
| Ana Rodríguez     | Colombia |
| Carlos Pérez      | Colombia |
| Luis Torres       | Colombia |
| Laura Pérez       | Colombia |
| Pedro Torres      | Colombia |
| Laura Rodríguez   | Colombia |
| Ana Pérez         | Colombia |
| Sofía Gómez       | Colombia |
| Pedro Pérez       | Colombia |
| Ana Gómez         | Colombia |
| Laura Torres      | Colombia |
| Carlos Torres     | Colombia |
| Pedro Rodríguez   | Colombia |
| Pedro Torres      | Colombia |
| Laura Torres      | Colombia |
+-------------------+----------+
100 rows in set (0.00 sec)
```



### 2.

**Enunciado:** Listar el nombre de cada cliente con su municipio, departamento y país.  

```sql
SELECT c.nombre,m.nombre,dp.nombre,p.nombre
FROM clientes c
JOIN municipio m ON c.municipioid = m.id
JOIN departamento dp ON m.depid = dp.id
JOIN pais p ON dp.paisid = p.id;
```

```
+----------------------+-----------------------+-----------------+----------+
| nombre               | municipio             | departamento    | pais     |
+----------------------+-----------------------+-----------------+----------+
| Valentina Mendoza    | Medellín              | Antioquia       | Colombia |
| Andrés Mendoza       | Medellín              | Antioquia       | Colombia |
| Daniela López        | Medellín              | Antioquia       | Colombia |
| Andrés Vargas        | Medellín              | Antioquia       | Colombia |
| Camila García        | Medellín              | Antioquia       | Colombia |
| Andrés Romero        | Medellín              | Antioquia       | Colombia |
| Valentina Hernández  | Medellín              | Antioquia       | Colombia |
| David Vargas         | Medellín              | Antioquia       | Colombia |
| Valentina López      | Medellín              | Antioquia       | Colombia |
| Julián López         | Medellín              | Antioquia       | Colombia |
| Sofía Martínez       | Bello                 | Antioquia       | Colombia |
| Andrés Mendoza       | Bello                 | Antioquia       | Colombia |
| Julián Hernández     | Bello                 | Antioquia       | Colombia |
| Daniela Vargas       | Bello                 | Antioquia       | Colombia |
| Daniela Hernández    | Bello                 | Antioquia       | Colombia |
| Sofía Rodríguez      | Bello                 | Antioquia       | Colombia |
| Valentina García     | Bello                 | Antioquia       | Colombia |
| Camila Vargas        | Bello                 | Antioquia       | Colombia |
| Daniela López        | Bello                 | Antioquia       | Colombia |
| Sofía López          | Bello                 | Antioquia       | Colombia |
| Julián García        | Itagüí                | Antioquia       | Colombia |
| David García         | Itagüí                | Antioquia       | Colombia |
| Andrés Mendoza       | Itagüí                | Antioquia       | Colombia |
| Daniela Vargas       | Itagüí                | Antioquia       | Colombia |
| David Rodríguez      | Itagüí                | Antioquia       | Colombia |
| Daniela García       | Itagüí                | Antioquia       | Colombia |
| Andrés García        | Itagüí                | Antioquia       | Colombia |
| David Romero         | Itagüí                | Antioquia       | Colombia |
| Julián Romero        | Itagüí                | Antioquia       | Colombia |
| Julián Mendoza       | Itagüí                | Antioquia       | Colombia |
| David Martínez       | Envigado              | Antioquia       | Colombia |
| Andrés Rodríguez     | Envigado              | Antioquia       | Colombia |
| David Rodríguez      | Envigado              | Antioquia       | Colombia |
| Juan Rodríguez       | Envigado              | Antioquia       | Colombia |
| Sofía López          | Envigado              | Antioquia       | Colombia |
| Camila López         | Envigado              | Antioquia       | Colombia |
| Camila López         | Envigado              | Antioquia       | Colombia |
| Andrés García        | Envigado              | Antioquia       | Colombia |
| Julián Rodríguez     | Envigado              | Antioquia       | Colombia |
| Julián Martínez      | Envigado              | Antioquia       | Colombia |
| Julián Mendoza       | Rionegro              | Antioquia       | Colombia |
| Andrés López         | Rionegro              | Antioquia       | Colombia |
| David Romero         | Rionegro              | Antioquia       | Colombia |
| Daniela García       | Rionegro              | Antioquia       | Colombia |
| Daniela Mendoza      | Rionegro              | Antioquia       | Colombia |
| Daniela García       | Rionegro              | Antioquia       | Colombia |
| Valentina Mendoza    | Rionegro              | Antioquia       | Colombia |
| Andrés Vargas        | Rionegro              | Antioquia       | Colombia |
| David García         | Rionegro              | Antioquia       | Colombia |
| Sofía Hernández      | Rionegro              | Antioquia       | Colombia |
| Valentina Mendoza    | Soacha                | Cundinamarca    | Colombia |
| Andrés Hernández     | Soacha                | Cundinamarca    | Colombia |
| Camila Hernández     | Soacha                | Cundinamarca    | Colombia |
| David Martínez       | Soacha                | Cundinamarca    | Colombia |
| Valentina Martínez   | Soacha                | Cundinamarca    | Colombia |
| Daniela Mendoza      | Soacha                | Cundinamarca    | Colombia |
| Andrés Martínez      | Soacha                | Cundinamarca    | Colombia |
| Sofía Mendoza        | Soacha                | Cundinamarca    | Colombia |
| Daniela Hernández    | Soacha                | Cundinamarca    | Colombia |
| Daniela García       | Soacha                | Cundinamarca    | Colombia |
| Sofía Martínez       | Chía                  | Cundinamarca    | Colombia |
| Juan Hernández       | Chía                  | Cundinamarca    | Colombia |
| David García         | Chía                  | Cundinamarca    | Colombia |
| Daniela Rodríguez    | Chía                  | Cundinamarca    | Colombia |
| Daniela Martínez     | Chía                  | Cundinamarca    | Colombia |
| Daniela Romero       | Chía                  | Cundinamarca    | Colombia |
| Daniela Martínez     | Chía                  | Cundinamarca    | Colombia |
| Andrés Romero        | Chía                  | Cundinamarca    | Colombia |
| Andrés Romero        | Chía                  | Cundinamarca    | Colombia |
| Valentina García     | Chía                  | Cundinamarca    | Colombia |
| Juan Vargas          | Zipaquirá             | Cundinamarca    | Colombia |
| Andrés López         | Zipaquirá             | Cundinamarca    | Colombia |
| Andrés López         | Zipaquirá             | Cundinamarca    | Colombia |
| Julián Vargas        | Zipaquirá             | Cundinamarca    | Colombia |
| Julián Mendoza       | Zipaquirá             | Cundinamarca    | Colombia |
| David García         | Zipaquirá             | Cundinamarca    | Colombia |
| David Hernández      | Zipaquirá             | Cundinamarca    | Colombia |
| Daniela Mendoza      | Zipaquirá             | Cundinamarca    | Colombia |
| Juan Vargas          | Zipaquirá             | Cundinamarca    | Colombia |
| Julián García        | Zipaquirá             | Cundinamarca    | Colombia |
| Camila Rodríguez     | Facatativá            | Cundinamarca    | Colombia |
| Valentina Vargas     | Facatativá            | Cundinamarca    | Colombia |
| Camila Vargas        | Facatativá            | Cundinamarca    | Colombia |
| Sofía Hernández      | Facatativá            | Cundinamarca    | Colombia |
| Andrés López         | Facatativá            | Cundinamarca    | Colombia |
| Andrés Hernández     | Facatativá            | Cundinamarca    | Colombia |
| Andrés Romero        | Facatativá            | Cundinamarca    | Colombia |
| Valentina Rodríguez  | Facatativá            | Cundinamarca    | Colombia |
| Valentina López      | Facatativá            | Cundinamarca    | Colombia |
| Camila Vargas        | Facatativá            | Cundinamarca    | Colombia |
| Valentina López      | Girardot              | Cundinamarca    | Colombia |
| Camila Romero        | Girardot              | Cundinamarca    | Colombia |
| Julián Rodríguez     | Girardot              | Cundinamarca    | Colombia |
| David Mendoza        | Girardot              | Cundinamarca    | Colombia |
| Daniela López        | Girardot              | Cundinamarca    | Colombia |
| Camila Mendoza       | Girardot              | Cundinamarca    | Colombia |
| Sofía García         | Girardot              | Cundinamarca    | Colombia |
| Valentina Romero     | Girardot              | Cundinamarca    | Colombia |
| Daniela Martínez     | Girardot              | Cundinamarca    | Colombia |
| Andrés Vargas        | Girardot              | Cundinamarca    | Colombia |
| Valentina López      | Cali                  | Valle del Cauca | Colombia |
| Julián Martínez      | Cali                  | Valle del Cauca | Colombia |
| Daniela García       | Cali                  | Valle del Cauca | Colombia |
| Camila Rodríguez     | Cali                  | Valle del Cauca | Colombia |
| Andrés Mendoza       | Cali                  | Valle del Cauca | Colombia |
| Juan López           | Cali                  | Valle del Cauca | Colombia |
| Juan Romero          | Cali                  | Valle del Cauca | Colombia |
| David García         | Cali                  | Valle del Cauca | Colombia |
| Camila Romero        | Cali                  | Valle del Cauca | Colombia |
| Sofía Martínez       | Cali                  | Valle del Cauca | Colombia |
| David López          | Palmira               | Valle del Cauca | Colombia |
| Julián Mendoza       | Palmira               | Valle del Cauca | Colombia |
| Camila Hernández     | Palmira               | Valle del Cauca | Colombia |
| Sofía Romero         | Palmira               | Valle del Cauca | Colombia |
| Juan Hernández       | Palmira               | Valle del Cauca | Colombia |
| Andrés Vargas        | Palmira               | Valle del Cauca | Colombia |
| Valentina Mendoza    | Palmira               | Valle del Cauca | Colombia |
| Andrés Romero        | Palmira               | Valle del Cauca | Colombia |
| Sofía Vargas         | Palmira               | Valle del Cauca | Colombia |
| Julián Romero        | Palmira               | Valle del Cauca | Colombia |
| Camila Vargas        | Buenaventura          | Valle del Cauca | Colombia |
| Daniela Vargas       | Buenaventura          | Valle del Cauca | Colombia |
| Valentina Mendoza    | Buenaventura          | Valle del Cauca | Colombia |
| David Romero         | Buenaventura          | Valle del Cauca | Colombia |
| David Vargas         | Buenaventura          | Valle del Cauca | Colombia |
| David Romero         | Buenaventura          | Valle del Cauca | Colombia |
| Camila López         | Buenaventura          | Valle del Cauca | Colombia |
| Sofía Hernández      | Buenaventura          | Valle del Cauca | Colombia |
| Julián Rodríguez     | Buenaventura          | Valle del Cauca | Colombia |
| Julián García        | Buenaventura          | Valle del Cauca | Colombia |
| Sofía Hernández      | Tuluá                 | Valle del Cauca | Colombia |
| Juan García          | Tuluá                 | Valle del Cauca | Colombia |
| David Vargas         | Tuluá                 | Valle del Cauca | Colombia |
| Andrés Hernández     | Tuluá                 | Valle del Cauca | Colombia |
| Daniela García       | Tuluá                 | Valle del Cauca | Colombia |
| Julián Vargas        | Tuluá                 | Valle del Cauca | Colombia |
| Valentina Romero     | Tuluá                 | Valle del Cauca | Colombia |
| Sofía López          | Tuluá                 | Valle del Cauca | Colombia |
| Sofía García         | Tuluá                 | Valle del Cauca | Colombia |
| Valentina Hernández  | Tuluá                 | Valle del Cauca | Colombia |
| Valentina López      | Cartago               | Valle del Cauca | Colombia |
| Camila Martínez      | Cartago               | Valle del Cauca | Colombia |
| Juan Romero          | Cartago               | Valle del Cauca | Colombia |
| Sofía Hernández      | Cartago               | Valle del Cauca | Colombia |
| Julián García        | Cartago               | Valle del Cauca | Colombia |
| Julián Mendoza       | Cartago               | Valle del Cauca | Colombia |
| David Vargas         | Cartago               | Valle del Cauca | Colombia |
| Andrés Vargas        | Cartago               | Valle del Cauca | Colombia |
| Juan López           | Cartago               | Valle del Cauca | Colombia |
| Juan López           | Cartago               | Valle del Cauca | Colombia |
| Valentina Mendoza    | Barranquilla          | Atlántico       | Colombia |
| Camila García        | Barranquilla          | Atlántico       | Colombia |
| David Martínez       | Barranquilla          | Atlántico       | Colombia |
| Sofía Martínez       | Barranquilla          | Atlántico       | Colombia |
| Daniela Vargas       | Barranquilla          | Atlántico       | Colombia |
| Juan Vargas          | Barranquilla          | Atlántico       | Colombia |
| Julián Hernández     | Barranquilla          | Atlántico       | Colombia |
| Valentina García     | Barranquilla          | Atlántico       | Colombia |
| Valentina Rodríguez  | Barranquilla          | Atlántico       | Colombia |
| Camila Martínez      | Barranquilla          | Atlántico       | Colombia |
| Julián López         | Soledad               | Atlántico       | Colombia |
| Valentina Romero     | Soledad               | Atlántico       | Colombia |
| Julián Hernández     | Soledad               | Atlántico       | Colombia |
| Daniela Hernández    | Soledad               | Atlántico       | Colombia |
| Sofía Rodríguez      | Soledad               | Atlántico       | Colombia |
| Daniela López        | Soledad               | Atlántico       | Colombia |
| Andrés Rodríguez     | Soledad               | Atlántico       | Colombia |
| Daniela Rodríguez    | Soledad               | Atlántico       | Colombia |
| Valentina Rodríguez  | Soledad               | Atlántico       | Colombia |
| Daniela Vargas       | Soledad               | Atlántico       | Colombia |
| David Hernández      | Malambo               | Atlántico       | Colombia |
| Sofía Rodríguez      | Malambo               | Atlántico       | Colombia |
| David Mendoza        | Malambo               | Atlántico       | Colombia |
| Daniela Romero       | Malambo               | Atlántico       | Colombia |
| Sofía García         | Malambo               | Atlántico       | Colombia |
| Juan Rodríguez       | Malambo               | Atlántico       | Colombia |
| Valentina García     | Malambo               | Atlántico       | Colombia |
| Camila Rodríguez     | Malambo               | Atlántico       | Colombia |
| David Mendoza        | Malambo               | Atlántico       | Colombia |
| Valentina Romero     | Malambo               | Atlántico       | Colombia |
| David Hernández      | Puerto Colombia       | Atlántico       | Colombia |
| Camila López         | Puerto Colombia       | Atlántico       | Colombia |
| Valentina Hernández  | Puerto Colombia       | Atlántico       | Colombia |
| David Hernández      | Puerto Colombia       | Atlántico       | Colombia |
| Valentina Mendoza    | Puerto Colombia       | Atlántico       | Colombia |
| Julián Hernández     | Puerto Colombia       | Atlántico       | Colombia |
| Juan López           | Puerto Colombia       | Atlántico       | Colombia |
| David García         | Puerto Colombia       | Atlántico       | Colombia |
| Julián Vargas        | Puerto Colombia       | Atlántico       | Colombia |
| Julián Hernández     | Puerto Colombia       | Atlántico       | Colombia |
| Sofía Vargas         | Sabanalarga           | Atlántico       | Colombia |
| Sofía López          | Sabanalarga           | Atlántico       | Colombia |
| Sofía Vargas         | Sabanalarga           | Atlántico       | Colombia |
| Valentina Mendoza    | Sabanalarga           | Atlántico       | Colombia |
| Julián Rodríguez     | Sabanalarga           | Atlántico       | Colombia |
| Julián Vargas        | Sabanalarga           | Atlántico       | Colombia |
| Juan López           | Sabanalarga           | Atlántico       | Colombia |
| Juan Mendoza         | Sabanalarga           | Atlántico       | Colombia |
| Valentina Romero     | Sabanalarga           | Atlántico       | Colombia |
| Sofía Martínez       | Sabanalarga           | Atlántico       | Colombia |
| Andrés Martínez      | Cartagena             | Bolívar         | Colombia |
| Camila García        | Cartagena             | Bolívar         | Colombia |
| Valentina Romero     | Cartagena             | Bolívar         | Colombia |
| Andrés López         | Cartagena             | Bolívar         | Colombia |
| Daniela López        | Cartagena             | Bolívar         | Colombia |
| Julián Romero        | Cartagena             | Bolívar         | Colombia |
| David López          | Cartagena             | Bolívar         | Colombia |
| Camila Rodríguez     | Cartagena             | Bolívar         | Colombia |
| Julián Martínez      | Cartagena             | Bolívar         | Colombia |
| Juan Rodríguez       | Cartagena             | Bolívar         | Colombia |
| Sofía Rodríguez      | Magangué              | Bolívar         | Colombia |
| David Rodríguez      | Magangué              | Bolívar         | Colombia |
| Daniela Hernández    | Magangué              | Bolívar         | Colombia |
| Daniela Mendoza      | Magangué              | Bolívar         | Colombia |
| David Romero         | Magangué              | Bolívar         | Colombia |
| Julián Rodríguez     | Magangué              | Bolívar         | Colombia |
| Daniela Romero       | Magangué              | Bolívar         | Colombia |
| Sofía Rodríguez      | Magangué              | Bolívar         | Colombia |
| Andrés Rodríguez     | Magangué              | Bolívar         | Colombia |
| Andrés Rodríguez     | Magangué              | Bolívar         | Colombia |
| Julián Rodríguez     | Turbaco               | Bolívar         | Colombia |
| Andrés Mendoza       | Turbaco               | Bolívar         | Colombia |
| Juan Vargas          | Turbaco               | Bolívar         | Colombia |
| David Hernández      | Turbaco               | Bolívar         | Colombia |
| Andrés Mendoza       | Turbaco               | Bolívar         | Colombia |
| Daniela Martínez     | Turbaco               | Bolívar         | Colombia |
| Daniela Hernández    | Turbaco               | Bolívar         | Colombia |
| Juan Mendoza         | Turbaco               | Bolívar         | Colombia |
| Julián Mendoza       | Turbaco               | Bolívar         | Colombia |
| Julián López         | Turbaco               | Bolívar         | Colombia |
| Andrés Martínez      | El Carmen de Bolívar  | Bolívar         | Colombia |
| Andrés López         | El Carmen de Bolívar  | Bolívar         | Colombia |
| Camila Mendoza       | El Carmen de Bolívar  | Bolívar         | Colombia |
| Daniela Martínez     | El Carmen de Bolívar  | Bolívar         | Colombia |
| Camila Romero        | El Carmen de Bolívar  | Bolívar         | Colombia |
| Valentina Rodríguez  | El Carmen de Bolívar  | Bolívar         | Colombia |
| Sofía Romero         | El Carmen de Bolívar  | Bolívar         | Colombia |
| Juan Rodríguez       | El Carmen de Bolívar  | Bolívar         | Colombia |
| Daniela Romero       | El Carmen de Bolívar  | Bolívar         | Colombia |
| Valentina García     | El Carmen de Bolívar  | Bolívar         | Colombia |
| Andrés Martínez      | Arjona                | Bolívar         | Colombia |
| Sofía Martínez       | Arjona                | Bolívar         | Colombia |
| Camila López         | Arjona                | Bolívar         | Colombia |
| Daniela García       | Arjona                | Bolívar         | Colombia |
| Daniela Vargas       | Arjona                | Bolívar         | Colombia |
| David Martínez       | Arjona                | Bolívar         | Colombia |
| Daniela Vargas       | Arjona                | Bolívar         | Colombia |
| Juan Vargas          | Arjona                | Bolívar         | Colombia |
| Daniela García       | Arjona                | Bolívar         | Colombia |
| Andrés Hernández     | Arjona                | Bolívar         | Colombia |
| David Vargas         | Bucaramanga           | Santander       | Colombia |
| David Hernández      | Bucaramanga           | Santander       | Colombia |
| Julián Romero        | Bucaramanga           | Santander       | Colombia |
| Andrés Vargas        | Bucaramanga           | Santander       | Colombia |
| Andrés Rodríguez     | Bucaramanga           | Santander       | Colombia |
| Valentina Hernández  | Bucaramanga           | Santander       | Colombia |
| Valentina Romero     | Bucaramanga           | Santander       | Colombia |
| David Hernández      | Bucaramanga           | Santander       | Colombia |
| Julián García        | Bucaramanga           | Santander       | Colombia |
| Daniela Vargas       | Bucaramanga           | Santander       | Colombia |
| Sofía Vargas         | Floridablanca         | Santander       | Colombia |
| Valentina Romero     | Floridablanca         | Santander       | Colombia |
| Juan Vargas          | Floridablanca         | Santander       | Colombia |
| Juan López           | Floridablanca         | Santander       | Colombia |
| Juan Mendoza         | Floridablanca         | Santander       | Colombia |
| Julián López         | Floridablanca         | Santander       | Colombia |
| Daniela Romero       | Floridablanca         | Santander       | Colombia |
| Daniela Romero       | Floridablanca         | Santander       | Colombia |
| Andrés Rodríguez     | Floridablanca         | Santander       | Colombia |
| Daniela Vargas       | Floridablanca         | Santander       | Colombia |
| Sofía Rodríguez      | Giron                 | Santander       | Colombia |
| Juan Mendoza         | Giron                 | Santander       | Colombia |
| Valentina Vargas     | Giron                 | Santander       | Colombia |
| Andrés García        | Giron                 | Santander       | Colombia |
| David Mendoza        | Giron                 | Santander       | Colombia |
| Julián García        | Giron                 | Santander       | Colombia |
| Andrés Hernández     | Giron                 | Santander       | Colombia |
| Andrés López         | Giron                 | Santander       | Colombia |
| Valentina Vargas     | Giron                 | Santander       | Colombia |
| Valentina López      | Giron                 | Santander       | Colombia |
| Juan Mendoza         | Piedecuesta           | Santander       | Colombia |
| Juan Hernández       | Piedecuesta           | Santander       | Colombia |
| Valentina Vargas     | Piedecuesta           | Santander       | Colombia |
| Julián Vargas        | Piedecuesta           | Santander       | Colombia |
| David Vargas         | Piedecuesta           | Santander       | Colombia |
| Valentina Vargas     | Piedecuesta           | Santander       | Colombia |
| David López          | Piedecuesta           | Santander       | Colombia |
| Daniela Romero       | Piedecuesta           | Santander       | Colombia |
| Valentina Mendoza    | Piedecuesta           | Santander       | Colombia |
| Camila Vargas        | Piedecuesta           | Santander       | Colombia |
| Julián Romero        | Barrancabermeja       | Santander       | Colombia |
| Valentina García     | Barrancabermeja       | Santander       | Colombia |
| Sofía Rodríguez      | Barrancabermeja       | Santander       | Colombia |
| Julián García        | Barrancabermeja       | Santander       | Colombia |
| Camila Mendoza       | Barrancabermeja       | Santander       | Colombia |
| Sofía Martínez       | Barrancabermeja       | Santander       | Colombia |
| Andrés Rodríguez     | Barrancabermeja       | Santander       | Colombia |
| Valentina López      | Barrancabermeja       | Santander       | Colombia |
| David Hernández      | Barrancabermeja       | Santander       | Colombia |
| Sofía Hernández      | Barrancabermeja       | Santander       | Colombia |
| Camila Hernández     | Pasto                 | Nariño          | Colombia |
| Valentina Vargas     | Pasto                 | Nariño          | Colombia |
| Valentina Hernández  | Pasto                 | Nariño          | Colombia |
| Andrés Romero        | Pasto                 | Nariño          | Colombia |
| Julián Vargas        | Pasto                 | Nariño          | Colombia |
| Andrés Romero        | Pasto                 | Nariño          | Colombia |
| David Hernández      | Pasto                 | Nariño          | Colombia |
| Julián Vargas        | Pasto                 | Nariño          | Colombia |
| Julián Martínez      | Pasto                 | Nariño          | Colombia |
| Daniela Rodríguez    | Pasto                 | Nariño          | Colombia |
| Sofía García         | Tumaco                | Nariño          | Colombia |
| Valentina Martínez   | Tumaco                | Nariño          | Colombia |
| Andrés García        | Tumaco                | Nariño          | Colombia |
| Juan Mendoza         | Tumaco                | Nariño          | Colombia |
| Daniela López        | Tumaco                | Nariño          | Colombia |
| Andrés García        | Tumaco                | Nariño          | Colombia |
| Valentina López      | Tumaco                | Nariño          | Colombia |
| Julián Vargas        | Tumaco                | Nariño          | Colombia |
| Julián Rodríguez     | Tumaco                | Nariño          | Colombia |
| David Romero         | Tumaco                | Nariño          | Colombia |
| Juan Hernández       | Ipiales               | Nariño          | Colombia |
| Juan Romero          | Ipiales               | Nariño          | Colombia |
| Daniela García       | Ipiales               | Nariño          | Colombia |
| Camila Vargas        | Ipiales               | Nariño          | Colombia |
| David López          | Ipiales               | Nariño          | Colombia |
| Camila Hernández     | Ipiales               | Nariño          | Colombia |
| Sofía Romero         | Ipiales               | Nariño          | Colombia |
| Valentina Hernández  | Ipiales               | Nariño          | Colombia |
| Valentina Vargas     | Ipiales               | Nariño          | Colombia |
| Daniela Rodríguez    | Ipiales               | Nariño          | Colombia |
| Julián Martínez      | Túquerres             | Nariño          | Colombia |
| Camila López         | Túquerres             | Nariño          | Colombia |
| Sofía López          | Túquerres             | Nariño          | Colombia |
| David Romero         | Túquerres             | Nariño          | Colombia |
| Andrés Mendoza       | Túquerres             | Nariño          | Colombia |
| Valentina Vargas     | Túquerres             | Nariño          | Colombia |
| Juan Martínez        | Túquerres             | Nariño          | Colombia |
| David Romero         | Túquerres             | Nariño          | Colombia |
| Juan Vargas          | Túquerres             | Nariño          | Colombia |
| David García         | Túquerres             | Nariño          | Colombia |
| Camila Romero        | Samaniego             | Nariño          | Colombia |
| Andrés Mendoza       | Samaniego             | Nariño          | Colombia |
| Sofía Rodríguez      | Samaniego             | Nariño          | Colombia |
| Juan López           | Samaniego             | Nariño          | Colombia |
| David Martínez       | Samaniego             | Nariño          | Colombia |
| Andrés Rodríguez     | Samaniego             | Nariño          | Colombia |
| Valentina Hernández  | Samaniego             | Nariño          | Colombia |
| David Mendoza        | Samaniego             | Nariño          | Colombia |
| Valentina Romero     | Samaniego             | Nariño          | Colombia |
| Valentina Rodríguez  | Samaniego             | Nariño          | Colombia |
| David Mendoza        | Manizales             | Caldas          | Colombia |
| Andrés López         | Manizales             | Caldas          | Colombia |
| Daniela García       | Manizales             | Caldas          | Colombia |
| Julián Hernández     | Manizales             | Caldas          | Colombia |
| Juan Vargas          | Manizales             | Caldas          | Colombia |
| Camila Hernández     | Manizales             | Caldas          | Colombia |
| Juan García          | Manizales             | Caldas          | Colombia |
| Camila Rodríguez     | Manizales             | Caldas          | Colombia |
| Sofía García         | Manizales             | Caldas          | Colombia |
| Andrés Vargas        | Manizales             | Caldas          | Colombia |
| Daniela Romero       | Villamaría            | Caldas          | Colombia |
| David Rodríguez      | Villamaría            | Caldas          | Colombia |
| Camila Rodríguez     | Villamaría            | Caldas          | Colombia |
| Julián Martínez      | Villamaría            | Caldas          | Colombia |
| Juan Rodríguez       | Villamaría            | Caldas          | Colombia |
| Julián Mendoza       | Villamaría            | Caldas          | Colombia |
| Sofía López          | Villamaría            | Caldas          | Colombia |
| Sofía Martínez       | Villamaría            | Caldas          | Colombia |
| Juan López           | Villamaría            | Caldas          | Colombia |
| Camila Rodríguez     | Villamaría            | Caldas          | Colombia |
| Juan Vargas          | Chinchiná             | Caldas          | Colombia |
| David López          | Chinchiná             | Caldas          | Colombia |
| Valentina Mendoza    | Chinchiná             | Caldas          | Colombia |
| Camila Mendoza       | Chinchiná             | Caldas          | Colombia |
| David López          | Chinchiná             | Caldas          | Colombia |
| Valentina García     | Chinchiná             | Caldas          | Colombia |
| Andrés Vargas        | Chinchiná             | Caldas          | Colombia |
| Julián Vargas        | Chinchiná             | Caldas          | Colombia |
| Juan López           | Chinchiná             | Caldas          | Colombia |
| Valentina Martínez   | Chinchiná             | Caldas          | Colombia |
| Valentina Vargas     | La Dorada             | Caldas          | Colombia |
| Julián López         | La Dorada             | Caldas          | Colombia |
| David López          | La Dorada             | Caldas          | Colombia |
| Camila Hernández     | La Dorada             | Caldas          | Colombia |
| Sofía García         | La Dorada             | Caldas          | Colombia |
| Daniela López        | La Dorada             | Caldas          | Colombia |
| Daniela García       | La Dorada             | Caldas          | Colombia |
| Julián García        | La Dorada             | Caldas          | Colombia |
| Sofía García         | La Dorada             | Caldas          | Colombia |
| Andrés García        | La Dorada             | Caldas          | Colombia |
| Daniela López        | Riosucio              | Caldas          | Colombia |
| David Rodríguez      | Riosucio              | Caldas          | Colombia |
| Sofía Hernández      | Riosucio              | Caldas          | Colombia |
| Julián López         | Riosucio              | Caldas          | Colombia |
| Sofía Mendoza        | Riosucio              | Caldas          | Colombia |
| Sofía García         | Riosucio              | Caldas          | Colombia |
| Julián Hernández     | Riosucio              | Caldas          | Colombia |
| David Romero         | Riosucio              | Caldas          | Colombia |
| Julián Mendoza       | Riosucio              | Caldas          | Colombia |
| Valentina García     | Riosucio              | Caldas          | Colombia |
| Juan Martínez        | Ibagué                | Tolima          | Colombia |
| Juan Mendoza         | Ibagué                | Tolima          | Colombia |
| Valentina García     | Ibagué                | Tolima          | Colombia |
| Juan López           | Ibagué                | Tolima          | Colombia |
| Valentina Hernández  | Ibagué                | Tolima          | Colombia |
| Daniela Vargas       | Ibagué                | Tolima          | Colombia |
| Daniela García       | Ibagué                | Tolima          | Colombia |
| Andrés García        | Ibagué                | Tolima          | Colombia |
| David Romero         | Ibagué                | Tolima          | Colombia |
| Julián Martínez      | Ibagué                | Tolima          | Colombia |
+----------------------+-----------------------+-----------------+----------+
410 rows in set (0.00 sec)
```



### 3.

**Enunciado:** Obtener los nombres de los empleados cuyo puesto existe en más de una sucursal.  

```sql
SELECT e.nombre, e.puesto
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id;
```

```
+-------------------+------------+
| nombre            | puesto     |
+-------------------+------------+
| Laura Rodríguez   | Cajero     |
| Ana Pérez         | Técnico    |
| Sofía Gómez       | Vendedor   |
| Pedro Pérez       | Vendedor   |
| Ana Gómez         | Cajero     |
| Laura Torres      | Cajero     |
| Carlos Torres     | Técnico    |
| Pedro Rodríguez   | Vendedor   |
| Pedro Torres      | Bodeguero  |
| Laura Torres      | Vendedor   |
| Laura Rodríguez   | Bodeguero  |
| Luis Torres       | Cajero     |
| Luis Rodríguez    | Supervisor |
| Ana Pérez         | Vendedor   |
| Ana Gómez         | Vendedor   |
| Sofía Torres      | Cajero     |
| Sofía Gómez       | Bodeguero  |
| Luis Rodríguez    | Vendedor   |
| Laura Pérez       | Vendedor   |
| Sofía Pérez       | Vendedor   |
| Pedro Gómez       | Vendedor   |
| Carlos Gómez      | Vendedor   |
| Ana Gómez         | Supervisor |
| Sofía Rodríguez   | Supervisor |
| Sofía Rodríguez   | Cajero     |
| Pedro Gómez       | Supervisor |
| Laura Gómez       | Cajero     |
| Carlos Pérez      | Técnico    |
| Carlos Pérez      | Vendedor   |
| Luis Pérez        | Bodeguero  |
| Laura Gómez       | Técnico    |
| Carlos Rodríguez  | Bodeguero  |
| Sofía Torres      | Técnico    |
| Laura Pérez       | Cajero     |
| Laura Gómez       | Bodeguero  |
| Carlos Torres     | Vendedor   |
| Luis Torres       | Técnico    |
| Pedro Rodríguez   | Bodeguero  |
| Sofía Torres      | Bodeguero  |
| Sofía Torres      | Supervisor |
| Luis Pérez        | Vendedor   |
| Luis Gómez        | Bodeguero  |
| Carlos Rodríguez  | Técnico    |
| Luis Rodríguez    | Técnico    |
| Ana Torres        | Supervisor |
| Pedro Rodríguez   | Cajero     |
| Luis Pérez        | Supervisor |
| Ana Rodríguez     | Cajero     |
| Luis Gómez        | Técnico    |
| Sofía Pérez       | Bodeguero  |
| Sofía Rodríguez   | Bodeguero  |
| Pedro Gómez       | Bodeguero  |
| Ana Pérez         | Supervisor |
| Ana Pérez         | Bodeguero  |
| Ana Rodríguez     | Supervisor |
| Carlos Pérez      | Supervisor |
| Ana Torres        | Cajero     |
| Ana Rodríguez     | Técnico    |
| Luis Torres       | Supervisor |
| Ana Torres        | Bodeguero  |
| Sofía Rodríguez   | Vendedor   |
| Carlos Rodríguez  | Supervisor |
| Ana Rodríguez     | Bodeguero  |
| Luis Torres       | Vendedor   |
| Laura Pérez       | Técnico    |
| Pedro Torres      | Cajero     |
| Carlos Torres     | Cajero     |
| Pedro Torres      | Técnico    |
| Luis Rodríguez    | Bodeguero  |
| Luis Pérez        | Técnico    |
| Sofía Gómez       | Supervisor |
+-------------------+------------+
71 rows in set (0.00 sec)
```



### 4.

**Enunciado:** Mostrar el total de empleados por municipio y el nombre del departamento al que pertenecen.  

```sql
SELECT m.nombre AS municipio, dp.nombre AS departamento, COUNT(e.empleado_id) AS total_empleados 
FROM empleados AS e
JOIN sucursal AS s ON e.sucursalid = s.id
JOIN municipio AS m ON s.municipioid = m.id
JOIN departamento AS dp ON m.depid = dp.id
GROUP BY dp.nombre;
```

```
+--------------+-----------------+-----------------+
| municipio    | departamento    | total_empleados |
+--------------+-----------------+-----------------+
| Bello        | Antioquia       |              10 |
| Soacha       | Cundinamarca    |              10 |
| Chía         | Cundinamarca    |              10 |
| Zipaquirá    | Cundinamarca    |              10 |
| Facatativá   | Cundinamarca    |              10 |
| Cartago      | Valle del Cauca |              10 |
| Barranquilla | Atlántico       |              10 |
| Malambo      | Atlántico       |              10 |
| Samaniego    | Nariño          |              10 |
| Ibagué       | Tolima          |              10 |
+--------------+-----------------+-----------------+
```

### 5.

**Enunciado:** Mostrar todos los municipios con sucursales activas (que tengan al menos un empleado).  

```sql
SELECT m.nombre
FROM empleados e
JOIN sucursal s ON e.sucursalid = s.id
JOIN municipio m ON s.municipioid = m.id
ORDER BY m.nombre;
```

```
+--------------+
| municipio    |
+--------------+
| Bello        |
| Soacha       |
| Chía         |
| Zipaquirá    |
| Facatativá   |
| Cartago      |
| Barranquilla |
| Malambo      |
| Samaniego    |
| Ibagué       |
+--------------+
```



---

## 🧮 Sección 2: Funciones Agregadas (5 problemas)

### 6.

**Enunciado:** Obtener los 5 municipios con mayor cantidad de empleados.  

```sql

```

```
+-------------+-----------------+
| municipio   | total_empleados |
+-------------+-----------------+
| Bello       |              10 |
| Soacha      |              10 |
| Chía        |              10 |
| Zipaquirá   |              10 |
| Facatativá  |              10 |
+-------------+-----------------+
```

### 7.

**Enunciado:** Calcular el salario promedio, máximo y mínimo por cada tipo de puesto.  

```sql

```

```
+------------+----------------+------------+------------+
| puesto     | promedio       | maximo     | minimo     |
+------------+----------------+------------+------------+
| Cajero     | 1851693.171333 | 2391482.85 | 1321321.62 |
| Técnico    | 1804687.653125 | 2192256.28 | 1350835.09 |
| Vendedor   | 1880258.288400 | 2378794.18 | 1331756.39 |
| Bodeguero  | 1857643.731250 | 2360108.22 | 1328451.38 |
| Supervisor | 1742417.661500 | 2245567.40 | 1344254.84 |
+------------+----------------+------------+------------+
```



### 8.

**Enunciado:** Mostrar las sucursales con al menos 2 empleados y salario promedio superior a 1.8 millones.  

```sql

```

```
+------------------+-------+----------------+
| nombre           | total | promedio       |
+------------------+-------+----------------+
| Sucursal Zona 1  |    10 | 1916484.849000 |
| Sucursal Zona 3  |    10 | 1807789.417000 |
| Sucursal Zona 4  |    10 | 1929583.595000 |
| Sucursal Zona 5  |    10 | 1847349.308000 |
| Sucursal Zona 6  |    10 | 1842813.252000 |
| Sucursal Zona 7  |    10 | 1854213.800000 |
| Sucursal Zona 10 |    10 | 1902034.541000 |
+------------------+-------+----------------+
```



### 9.

**Enunciado:** Obtener el total de clientes por país.  

```sql

```

```
+----------+----------------+
| pais     | total_clientes |
+----------+----------------+
| Colombia |            410 |
+----------+----------------+
```

### 10.

**Enunciado:** Listar todos los puestos y el número de municipios diferentes donde se encuentran empleados con ese puesto.  

```sql

```

---

## 🧠 Sección 3: Subconsultas (5 problemas)

### 11.

**Enunciado:** Mostrar los nombres de los empleados que ganan más que el salario promedio de todos los supervisores.  

```sql

```

```
+------------+----------------------+
| puesto     | municipios_distintos |
+------------+----------------------+
| Bodeguero  |                    9 |
| Cajero     |                    8 |
| Supervisor |                    8 |
| Técnico    |                    9 |
| Vendedor   |                    9 |
+------------+----------------------+
5 rows in set (0.00 sec)
```

### 12.

**Enunciado:** Listar los municipios que no tienen empleados con el puesto de 'Cajero'.  

```sql
SELECT 
FROM empleados e
WHERE empleados IN (
	SELECT m.nombre
    FROM sucursal s
    JOIN municipio m ON s.municipio = m.id
    WHERE e.puesto = 'Cajero'
);
```

```
+-----------------------+
| nombre                |
+-----------------------+
| Medellín              |
| Itagüí                |
| Envigado              |
| Rionegro              |
| Facatativá            |
| Girardot              |
| Cali                  |
| Palmira               |
| Buenaventura          |
| Tuluá                 |
| Barranquilla          |
| Soledad               |
| Puerto Colombia       |
| Sabanalarga           |
| Cartagena             |
| Magangué              |
| Turbaco               |
| El Carmen de Bolívar  |
| Arjona                |
| Bucaramanga           |
| Floridablanca         |
| Giron                 |
| Piedecuesta           |
| Barrancabermeja       |
| Pasto                 |
| Tumaco                |
| Ipiales               |
| Túquerres             |
| Manizales             |
| Villamaría            |
| Chinchiná             |
| La Dorada             |
| Riosucio              |
| Espinal               |
| Melgar                |
| Honda                 |
| Líbano                |
| Tunja                 |
| Duitama               |
| Sogamoso              |
| Chiquinquirá          |
| Moniquirá             |
+-----------------------+
```

### 13.

**Enunciado:** Obtener los clientes que residen en municipios donde los empleados ganan mas de 1.9 millones en promedio.  

```sql

```

```
+----------------------+
| nombre               |
+----------------------+
| Valentina Mendoza    |
| Andrés Hernández     |
| Camila Hernández     |
| David Martínez       |
| Valentina Martínez   |
| Daniela Mendoza      |
| Andrés Martínez      |
| Sofía Mendoza        |
| Daniela Hernández    |
| Daniela García       |
| David Hernández      |
| Sofía Rodríguez      |
| David Mendoza        |
| Daniela Romero       |
| Sofía García         |
| Juan Rodríguez       |
| Valentina García     |
| Camila Rodríguez     |
| David Mendoza        |
| Valentina Romero     |
| Juan Martínez        |
| Juan Mendoza         |
| Valentina García     |
| Juan López           |
| Valentina Hernández  |
| Daniela Vargas       |
| Daniela García       |
| Andrés García        |
| David Romero         |
| Julián Martínez      |
+----------------------+
```



### 14.

**Enunciado:** Mostrar los nombres de los puestos cuyo salario máximo supera el salario promedio general.  

```sql

```

```
+------------+
| puesto     |
+------------+
| Cajero     |
| Técnico    |
| Vendedor   |
| Bodeguero  |
| Supervisor |
+------------+
```

### 15.

**Enunciado:** Listar los empleados que trabajan en municipios donde hay más de 9 clientes.  

```sql
SELECT
FROM empleados e
WHERE empleado_id
```

```
+-------------------+
| nombre            |
+-------------------+
| Sofía Pérez       |
| Pedro Gómez       |
| Carlos Gómez      |
| Ana Gómez         |
| Sofía Rodríguez   |
| Sofía Rodríguez   |
| Pedro Gómez       |
| Laura Gómez       |
| Carlos Pérez      |
| Carlos Pérez      |
| Carlos Torres     |
| Sofía Rodríguez   |
| Sofía Torres      |
| Sofía Pérez       |
| Ana Gómez         |
| Pedro Rodríguez   |
| Pedro Torres      |
| Luis Rodríguez    |
| Luis Pérez        |
| Sofía Gómez       |
| Carlos Pérez      |
| Ana Torres        |
| Ana Rodríguez     |
| Luis Rodríguez    |
| Luis Torres       |
| Sofía Gómez       |
| Laura Rodríguez   |
| Ana Gómez         |
| Ana Torres        |
| Luis Pérez        |
| Laura Rodríguez   |
| Luis Torres       |
| Luis Rodríguez    |
| Ana Pérez         |
| Ana Gómez         |
| Sofía Torres      |
| Sofía Gómez       |
| Luis Rodríguez    |
| Laura Pérez       |
| Sofía Gómez       |
| Carlos Torres     |
| Laura Gómez       |
| Luis Gómez        |
| Sofía Pérez       |
| Sofía Rodríguez   |
| Pedro Gómez       |
| Ana Pérez         |
| Ana Pérez         |
| Sofía Torres      |
| Ana Rodríguez     |
| Sofía Rodríguez   |
| Luis Rodríguez    |
| Luis Gómez        |
| Ana Torres        |
| Pedro Rodríguez   |
| Luis Pérez        |
| Ana Rodríguez     |
| Laura Pérez       |
| Pedro Rodríguez   |
| Ana Gómez         |
| Sofía Torres      |
| Ana Gómez         |
| Sofía Torres      |
| Luis Pérez        |
| Luis Rodríguez    |
| Luis Gómez        |
| Laura Torres      |
| Laura Torres      |
| Carlos Rodríguez  |
| Luis Rodríguez    |
| Luis Pérez        |
| Laura Gómez       |
| Carlos Rodríguez  |
| Sofía Torres      |
| Laura Pérez       |
| Laura Gómez       |
| Sofía Rodríguez   |
| Carlos Torres     |
| Luis Torres       |
| Pedro Rodríguez   |
| Sofía Gómez       |
| Luis Gómez        |
| Sofía Rodríguez   |
| Carlos Rodríguez  |
| Sofía Gómez       |
| Ana Rodríguez     |
| Carlos Pérez      |
| Luis Torres       |
| Laura Pérez       |
| Pedro Torres      |
| Laura Rodríguez   |
| Ana Pérez         |
| Sofía Gómez       |
| Pedro Pérez       |
| Ana Gómez         |
| Laura Torres      |
| Carlos Torres     |
| Pedro Rodríguez   |
| Pedro Torres      |
| Laura Torres      |
+-------------------+
```

