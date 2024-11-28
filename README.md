# Info_lesson-59
1. Процедуры — это именованные фрагменты кода, которые выполняют определённую задачу. Они позволяют структурировать программу, повторно использовать код и улучшать его читаемость
2. могут оформляться как "Процедура имя(параметры) ... КонецПроцедуры". В Паскале они оформляются аналогично с ключевым словом "procedure":
3. Нет, нужно также вызвать процедуру в тексте основной программы. В противном случае код процедуры не выполнится
4. это значения, которые передаются в процедуру. Они позволяют обрабатывать входные данные и делать процедуру более универсальной
5. Локальные переменные объявляются внутри процедуры и доступны только в пределах этой процедуры.
6. Процедуры с несколькими параметрами оформляются, перечисляя параметры через запятую в заголовке процедуры
7. Изменяемые параметры позволяют процедуре изменять значения переменных, переданных ей в качестве аргументов.
8. В Питоне все параметры неизменяемые по умолчанию, кроме объектов. В Паскале изменяемые параметры обозначаются ключевым словом "var":
9. В школьном алгоритмическом языке можно выделить простые, массивные и структурные параметры. Они объявляются через соответствующий тип данных.


ЗАДАЧИ

1.  procedure PrintOctalNumber(num: Integer);
 begin
     if num < 810 then
         WriteLn(Octal(num));
 end;

2. procedure PrintHexadecimalNumber(num: Integer);
begin
    if num < 65536 then
        WriteLn(Hex(num));
end;

3. procedure PrintStarSquare(N: Integer);
var
    i, j: Integer;
begin
    for i := 1 to N do
    begin
        for j := 1 to N do
            Write('*');
        WriteLn;
    end;
end;

4. procedure PrintAge(age: Integer);
begin
    if (age mod 10 = 1) and (age mod 100 <> 11) then
        WriteLn(age, ' год')
    else if (age mod 10 >= 2) and (age mod 10 <= 4) and (age mod 100 <> 12) and (age mod 100 <> 13) and (age mod 100 <> 14) then
        WriteLn(age, ' года')
    else
        WriteLn(age, ' лет');
end;

5.  procedure PrintNumberInWords(num: Integer);
begin
// Реализация вывода числа прописью
end;

6.  procedure PrintFibonacci(N: Integer);
var
    a, b, temp, i: Integer;
begin
    a := 0;
    b := 1;
    for i := 1 to N do
    begin
        Write(a, ' ');
        temp := a;
        a := b;
        b := temp + b;
    end;
end;

7.  procedure CheckPrime(var num: Integer; var isPrime: Boolean);
var
    i: Integer;
begin
    isPrime := True;
    if num < 2 then isPrime := False;
    for i := 2 to Trunc(Sqrt(num)) do
        if (num mod i = 0) then
        begin
            isPrime := False;
            Break;
        end;
end;

8.  procedure PrintDigitsReversed(num: Integer);
begin
    while num > 0 do
    begin
        WriteLn(num mod 10);
        num := num div 10;
    end;
end;

9.   procedure PrintDigitsForward(num: Integer);
var
    digits: array of Integer;
    i: Integer;
begin
    while num > 0 do
    begin
        SetLength(digits, Length(digits) + 1);
        digits[High(digits)] := num mod 10;
        num := num div 10;
    end;
    for i := High(digits) downto 0 do
        WriteLn(digits[i]);
end;

10.    procedure PrintDivisors(num: Integer);
var
    i: Integer;
begin
    for i := 1 to num do
        if (num mod i = 0) then
            Write(i, ' ');
    WriteLn;
end;

11.   procedure PrintLine(M: Integer);
var
    i: Integer;
begin
    for i := 1 to M do
        Write('-');
    WriteLn;
end;

12.  procedure PrintRoman(num: Integer);
var
    roman: array[1..13] of String = ('I', 'II', 'III', 'IV', 'V', 'VI', 
                                       'VII', 'VIII', 'IX', 'X', 'L', 'C', 'D', 'M');
begin
    // Реализация для преобразования числа в римские цифры
end;

