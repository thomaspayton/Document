# Document
using System;
using System.IO;

namespace Documents
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            Console.WriteLine("Document\n");

            Console.WriteLine("Document name:");
            string name1 = Console.ReadLine()+ ".txt";

            Console.WriteLine("Content for {0}:", name1);
            string cont = Console.ReadLine();
            //string folderPath = System.IO.Path.GetDirectoryName(Assembly.GetEntryAssembly().Location);

            StreamWriter sw = new StreamWriter(name1);

            string line = "";

            using (StreamReader sr = new StreamReader("c:/name1"))
            {
                while ((line = sr.ReadLine()) != null)
                {
                    Console.WriteLine(line);
                }
                Console.ReadKey();
            }
        }
    }

}

