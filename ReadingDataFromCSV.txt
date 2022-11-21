using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.IO;

namespace ReadingDataFromCSV
{
    internal class Program
    {
        static void Main(string[] args)
        {
            String filePath = @"C:\Users\LIKITHA\Desktop\enverus\Oct2022.csv";
            try
            {
                using (StreamReader reader = new StreamReader(filePath))
                {
                    string line;
                    while((line = reader.ReadLine()) != null)
                    {
                        Console.WriteLine(line);
                    }
                }
            }
            catch(Exception e)
            {
                Console.WriteLine(e.Message);
            }
            Console.ReadKey();
        }
    }
}
