### Índice
[[#1 - Tipos de Datos]]
[[#2 - Operadores Lógicos]]
[[#3 - Estructuras de Control]]
	[[#3.1 - IF]]
	[[#3.2 - While]]
	[[#3.3 - Repeat Until]]
	[[#3.4 - For]]
[[#4 - Procedimientos Y Funciones]]
	[[#4.1 - Procedure]]
	[[#4.2 - Function]]
[[#5 - Registros]]
	[[#5.1 - Register]]
[[#6 - Arreglos (Vectores)]]
	[[#6.1 - Declaración]]
	[[#6.2 - Recorrido]]
[[#7 - Punteros]]
	[[#7.1 - Declaración]]
	[[#7.2 - Asignación dinámica]]
[[#8 - Estructuras Recomendadas]]
	[[#8.1 - Condiciones de Corte]]
		[[#8.1.1 - Por valor de dato]]
		[[#8.1.2 - Por Repeat]]
	[[#8.2 - Acumuladores y Contadores]]
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
#### 7.1 - Declaración
```
type
  puntero = ^integer;
var
  p: puntero;
```
#### 7.2 - Asignación dinámica
```
new(p);
p^ := 25;
dispose(p);
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
