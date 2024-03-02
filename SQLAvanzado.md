## Subconsultas

Subconsultas, tambien onocidas como, _subqueries_, son una herramienta avanzas en SQL. Estas permiten enlazar consultas una dentro de otras, permitiendo la extracción eficiente de datos en sutuaciones complejas. De esta manera podemos tener mayor flexibilidad a la hora de realizar analisis de datos de manera mas sofisticada, podemos filtrar un numero elevado de datos de manera eficiente y eoptimizar las consultas de manera de mejorar el rendmiento general.

La integracion de subconsultas se relizan en comandos tales como **WHERE**, **HAVING**, **SELECT** y **FROM**


| Tipo de Subconsulta             | Descripción                                        |
|---------------------------------|----------------------------------------------------|
| Scalar Subqueries               | Subconsultas que devuelven un solo valor (escalar). Por ejemplo, `(SELECT COUNT(*) FROM table)`.                                                                                   |
| Comparisons using subqueries    | Subconsultas utilizadas en comparaciones, como `WHERE column = (SELECT column FROM table)`.                               |
| Row subqueries                  | Subconsultas que devuelven un conjunto de filas, se utilizan en contextos donde se espera una fila. Ejemplo: `SELECT * FROM table WHERE (column1, column2) = (SELECT col1, col2 FROM other_table)`.                |
| Exists and not exists subqueries| Subconsultas utilizadas con `EXISTS` o `NOT EXISTS` para verificar la existencia de filas en una subconsulta. Por ejemplo, `SELECT * FROM table WHERE EXISTS (SELECT * FROM other_table WHERE condition)`.  |
| Any in some subqueries          | Subconsultas utilizadas con `ANY`, `IN`, o `SOME` para comparar valores con un conjunto de valores devuelto por una subconsulta. Ejemplo: `SELECT * FROM table WHERE column > ANY (SELECT column FROM other_table)`. |
| All subqueries                  | Subconsultas utilizadas con `ALL` para comparar un valor con todos los valores devueltos por una subconsulta. Ejemplo: `SELECT * FROM table WHERE column > ALL (SELECT column FROM other_table)`.        |

## Scalar subqueries

  SELECT (SELECT s2 FROM t1);
