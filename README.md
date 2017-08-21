# Special-Numbers
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Special_Numbers
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            for (int i = 1; i <= n; i++)
            {
                string specialNum = String.Empty;

                if (i < 10)
                {
                    if (i == 5 || i == 7 || i == 11)
                    {
                        specialNum = "True";     
                    }
                    else
                    {
                        specialNum = "False";
                    }
                }
                else
                {
                    int firstDigit = i / 10;
                    int lastDigit = i % 10;

                    int sum = firstDigit + lastDigit;

                    if (sum == 5 || sum == 7 || sum == 11)
                    {
                        specialNum = "True";
                    }
                    else
                    {
                        specialNum = "False";
                    }
                }

                Console.WriteLine($"{i} -> {specialNum}");
            }
        }
    }
}
