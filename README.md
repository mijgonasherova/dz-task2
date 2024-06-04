// Задача 2: Напишите программу вычисления функции Аккермана с помощью рекурсии. 
// Даны два неотрицательных числа m и n.
// Пример
// m = 2, n = 3 -> A(m,n) = 29

using System;
class Program
{
    static int A(int m, int n)
    {
        if (m == 0)
        {
            return n + 1;
        }
        else if (n == 0)
        {
            return A(m - 1, 1);
        }
        else
        {
            return A(m - 1, A(m, n - 1));
        }
    }
    static void Main()
    {
        int m = 2;
        int n = 3;

        int result = A(n, m) ;
        Console.WriteLine($"A({m}, {n}) = {result}");
    }
}
