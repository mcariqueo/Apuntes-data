## Subconsultas

Subconsultas, tambien onocidas como, _subqueries_, son una herramienta avanzas en SQL. Estas permiten enlazar consultas una dentro de otras, permitiendo la extracción eficiente de datos en sutuaciones complejas. De esta manera podemos tener mayor flexibilidad a la hora de realizar analisis de datos de manera mas sofisticada, podemos filtrar un numero elevado de datos de manera eficiente y eoptimizar las consultas de manera de mejorar el rendmiento general.

La integracion de subconsultas se relizan en comandos tales como **WHERE**, **HAVING**, **SELECT** y **FROM**

<details>
	<summary>Tabla completa</summary>

| Tipo de Subconsulta             | Descripción                                       | Ejemplo                                               |
|---------------------------------|---------------------------------------------------|-------------------------------------------------------|
| Scalar                          | Devuelven un solo valor (escalar).                | `(SELECT COUNT(*) FROM table)`                       |
| Comparisons                     | Usadas en comparaciones.                          | `WHERE column = (SELECT column FROM table)`          |
| Row                             | Devuelven un conjunto de filas.                   | `SELECT * FROM table WHERE (column1, column2) = (SELECT col1, col2 FROM other_table)` |
| Exists and not exists subqueries| Utilizadas con `EXISTS` o `NOT EXISTS`.           | `SELECT * FROM table WHERE EXISTS (SELECT * FROM other_table WHERE condition)` |
| Any in some subqueries          | Usadas con `ANY`, `IN`, o `SOME`.                 | `SELECT * FROM table WHERE column > ANY (SELECT column FROM other_table)` |
| All subqueries                  | Usadas con `ALL` para comparar valores.           | `SELECT * FROM table WHERE column > ALL (SELECT column FROM other_table)` |

</details>

## Scalar subqueries

    SELECT (SELECT s2 FROM t1);

Mediante este comando es posible obtener unn valor unico. Esto se llama, valor escalar.






