# oscarMergeArray

using System;

namespace mergingArray
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] leftArray = new int[] { 1, 1, 3, 4, 5 };
            int[] rightArray = new int[] { 2, 4, 5, 6, 9 };
            int[] bigArray = new int[leftArray.Length + rightArray.Length];
            int tla = 0;
            int tra = 0;
            int i = 0;
            int j = 0;

            for (i = 0; i < bigArray.Length; i++)
            {
                if (leftArray[tla] <= rightArray[tra] && tla<leftArray.Length && tra<rightArray.Length)
                {
                    bigArray[i] = leftArray[tla];
                    if (tla < leftArray.Length-1)
                    {
                        tla++;
                    }
                }
                else if (rightArray[tra] < leftArray[tla] && tla<leftArray.Length && tra<rightArray.Length)
                {
                    bigArray[i] = rightArray[tra];
                    tra++;
                }
                ////else if (leftArray.Length-1 == tla)
                ////{
                ////    bigArray[i] = rightArray[tra];
                ////    tra++;
                ////}
                ////else if (rightArray.Length - 1 == tra)
                ////{
                ////    bigArray[i] = leftArray[tla];
                ////    tla++;
                ////}
            }
            for (j = 0; j < bigArray.Length; j++)
            {
                Console.WriteLine(bigArray[j]);
                Console.ReadLine();
            }
        }
    }
}
