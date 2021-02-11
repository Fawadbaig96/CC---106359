# Group Members

## Fawad Baig (62669)
## Sameen Azhar (63358)

# Regular Expression

(a+b)(a+b+0+1+_+.)*@(a+b+0+1+.)*


# NFA for the RE



![12](https://user-images.githubusercontent.com/66685640/107610071-8d691100-6c62-11eb-89f5-8a7b2a9ea1ae.jpg)


# Table

![image](https://user-images.githubusercontent.com/71581109/107633432-d4b6c800-6c89-11eb-83c9-a4ecf589491a.png)

# DFA

![WhatsApp Image 2021-02-11 at 10 21 52 AM](https://user-images.githubusercontent.com/71581109/107633617-24958f00-6c8a-11eb-9392-bb45ef4c8c05.jpeg)

# Code

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace AutomataProject_Spring_20
{
    class Program
    {
        static void Main(string[] args)
        {

          (a+b)(a+b+0+1+_+.)*@(a+b+0+1+.)*

            //////////////////////// TRANSITION TABLE /////////////////////////////////////////
            Dictionary<int, Dictionary<char, int>> dfa = new Dictionary<int, Dictionary<char, int>>()
            {
                {
                  //Current State           //next_state_for 'a'       //next_state_for 'b'
                     0,new Dictionary<char, int>{  { 'a', 2 } ,               {'b',2} }
                },
                {
                     1,new Dictionary<char, int>{{ 'a', 2 } ,                {'0',3} }
                },
                {
                     2,new Dictionary<char, int>{{ 'b', 2 } ,                {'1',3} }
                },
                {
                     3,new Dictionary<char



 public static bool accepts(Dictionary<int, Dictionary<char, int>> transitions, int initial, int[] arr ,string s)
        {
            int state = initial;
            bool final;
            Console.WriteLine("current_state\tcharacter\tnext_state");
            foreach (char c in s)
            {
                if (c != 'a' && c != 'b')
                {
                    Console.WriteLine($"{c} is not a part of language {{a,b}}");
                    return false;
                }
                Console.Write(state+"\t\t"); //to print the transitions
                state = transitions[state][c];
                Console.WriteLine( c + "\t\t"+ state );
                
            }
               
            return final  = true ? arr.Contains(state) : false;
        }
        public static string random()
        {
            
           string s = "";
            Random r = new Random(DateTime.Now.Millisecond);
            int length = r.Next(3,11);
            for (int i = 0; i < length; i++)
            {
                int w = r.Next(97,99);
                s += (char)w;
            }

            
            //=r.Next(97, 98);

            return s;
        }

    }
}
