[1 - Tipos de Datos](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#1---tipos-de-datos)

[2 - Operadores Logicos](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#2---operadores-logicos)

[3 - Estructuras de Control](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#3---estructuras-de-control)

[4 - Procedimientos y Funciones](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#4---procedimientos-y-funciones)

[5 - Registros](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#5---registros)

[6 - Arreglos (Vectores)](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#6---arreglos-(vectores))

[7 - Punteros](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#7---punteros)

[8- Estructuras Recomendadas](https://github.com/Julian-Gonzalez-Gomez/Documentacion-Free-Pascal-?tab=readme-ov-file#8---estructuras-recomendadas)

]
### 1 - Tipos de Datos

| Sintaxis | Dato                 |
| -------- | -------------------- |
| real     | reales               |
| string   | cadena de caracteres |
| boolean  | true/false           |
| char     | caracteres           |
| integer  | enteros              |
#### Constante
```
const
  PI = 3.1415;
```
#### Subrango
```
type
  rango = 1..10;
```
### 2 - Operadores Lógicos

| Aritméticos:      | `+`, `-`, `*`, `/`, `div`, `mod` |
| ----------------- | -------------------------------- |
| **Relacionales:** | `=`, `<>`, `<`, `<=`, `>`, `>=`  |
| **Lógicos:**      | `and`, `or`, `not`               |
### 3 - Estructuras de Control
#### 3.1 - IF
```
if (condición) then
  instrucción
else
  instrucción;
```
#### 3.2 - While
```
repeat
  instrucción;
until (condición);
```
#### 3.3 - Repeat Until
```
repeat
  instrucción;
until (condición);
```
2#### 3.4 - For
```
for i := 1 to 10 do
  instrucción;
```
### 4 - Procedimientos Y Funciones
#### 4.1 - Procedure
```
procedure nombreProcedimiento(var parametro: integer);
begin
  { instrucciones }
end;
```
#### 4.2 - Function
```
function nombreFuncion(x, y: integer): integer;
begin
  nombreFuncion := x + y;
end;
```
#### Uso de Parámetros
##### Por valor (se copia el valor)
```
procedure suma(a, b: integer);
```
##### Por referencia (se pasa la dirección de memoria)
```
procedure suma(var a, b: integer);
```


### 5 - Registros
#### 5.1 - Register
```
type
  alumno = record
    codigo: integer;
    nombre: string[20];
    promedio: real;
  end;
```
### 6 - Arreglos (Vectores)
#### 6.1 - Declaración
```
type
  vector = array[1..100] of integer;
```
#### 6.2 - Recorrido
```
for i := 1 to dimL do
  writeln(vector[i]);
```
### 7 - Punteros
#### Sintaxis
```
puntero_cadena = ^string/integer/real/boolean/regiter/array;
```
```
p: puntero_producto;
```
#### Instruciones
New
```
new(p);
```
Depose
```
dispose(p);
```
Sizeof
```
writeln(sizeof(p^), ' bytes'); imprime 8/4 bytes
writeln(sizeof(p), ' bytes');  imprime el tamaño de lo que 'p' contenga
```
### 8 - Estructuras Recomendadas
#### 8.1 - Condiciones de Corte
##### 8.1.1 - Por valor de dato
```
while (codigo <> 0) do
begin
  read(codigo);
end;
```
##### 8.1.2 - Por Repeat
```
repeat
  read(numero);
until (numero = 100);
```
#### 8.2 - Acumuladores y Contadores
```
total := 0;
cant := 0;
while (condicion) do
begin
  total := total + valor;
  cant := cant + 1;
end;
```
