using System;

namespace _09.PalindromeIntegers
{
    class Program
    {
        static void Main(string[] args)
        {
           string n = Console.ReadLine();
            while (n != "END")
            {
                bool isIntegerPalindrome = ReturnIsNumberPalindrome(n);
                if (isIntegerPalindrome)
                {
                    Console.WriteLine("true");
                }
                else
                {
                    Console.WriteLine("false");
                }
                n = Console.ReadLine();
            }
        }

        private static bool ReturnIsNumberPalindrome(string n)
        {
            int number = int.Parse(n);
            bool result = false;
            if (number >=0 && number <= 9)
            {
                return true;
            }
            else
            {
                for (int i =0; i < n.Length/2;i++)
                {
                    if (n[i] == n[n.Length -1])
                    {
                        result = true;
                    }
                    else
                    {
                        break;
                    }
                }
            }
            return result;

        }
    }
}
