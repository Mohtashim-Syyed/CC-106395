### MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim Kamal** <!--this is the group leader in bold-->
63433 | Yousuf Muhammad Khan


#### Given:  Alphabet = {"a", "b", "0", "1", ".", "_", "@"}

#### REGULAR EXPRESSION FOR GIVEN Alphabet: (a+b)(a+b+0+1+.+_)*@(a+b+0+1+.)*

#### NFA FOR R.E ####

![WhatsApp Image 2021-02-11 at 10 30 05 AM](https://user-images.githubusercontent.com/61554600/107605177-378d6c80-6c54-11eb-99ee-e8c1a792f503.jpeg)

### DFA from NFA ###

| NFA State                    | DFA State | a                            | b                            | 0                            | 1                            | _                            |  "."                         | @                         |
|------------------------------|-----------|------------------------------|------------------------------|------------------------------|------------------------------|------------------------------|------------------------------|---------------------------|
| {1,2,3}                      | A         | {5,6,7,8,9,10,11,12,13,21}   | {4,6,7,8,9,10,11,12,13,21}   | -                            | -                            | -                            | -                            | -                         |
| {5,6,7,8,9,10,11,12,13,21}   | B         | {14,20,21,7,8,9,10,11,12,13} | {15,20,21,7,8,9,10,11,12,13} | {16,20,21,7,8,9,10,11,12,13} | {17,20,21,7,8,9,10,11,12,13} | {18,20,21,7,8,9,10,11,12,13} | {19,20,21,7,8,9,10,11,12,13} | {22,23,24,25,26,27,28,35} |
| {4,6,7,8,9,10,11,12,13,21}   | C         | D                            | E                            | F                            | G                            | H                            | I                            | J                         |
| {14,20,21,7,8,9,10,11,12,13} | D         | D                            | E                            | F                            | G                            | H                            | I                            | j                         |
| {15,20,21,7,8,9,10,11,12,13} | E         | D                            | E                            | F                            | G                            | H                            | I                            | j                         |
| {16,20,21,7,8,9,10,11,12,13} | F         | D                            | E                            | F                            | G                            | H                            | I                            | j                         |
| {17,20,21,7,8,9,10,11,12,13} | G         | D                            | E                            | F                            | G                            | H                            | I                            | j                         |
| {18,20,21,7,8,9,10,11,12,13} | H         | D                            | E                            | F                            | G                            | H                            | I                            | j                         |
| {19,20,21,7,8,9,10,11,12,13} | I         | D                            | E                            | F                            | G                            | H                            | I                            | j                         |
| {22,23,24,25,26,27,28,35}    | J         | 29,34,35,23,24,25,26,27,28   | 30,34,35,23,24,25,26,27,28   | 31,34,35,23,24,25,26,27,28   | 32,34,35,23,24,25,26,27,28   | -                            | 33,34,35,23,24,25,26,27,28   | -                         |
| 29,34,35,23,24,25,26,27,28   | K         | K                            | L                            | M                            | N                            | -                            | O                            | -                         |
| 30,34,35,23,24,25,26,27,28   | L         | K                            | L                            | M                            | N                            | -                            | O                            | -                         |
| 31,34,35,23,24,25,26,27,28   | M         | K                            | L                            | M                            | N                            | -                            | O                            | -                         |
| 32,34,35,23,24,25,26,27,28   | N         | K                            | L                            | M                            | N                            | -                            | O                            | -                         |
| 33,34,35,23,24,25,26,27,28   | O         | K                            | L                            | M                            | N                            | -                            | O                            | -                         |


### CODE ###

using System;

using System.Collections.Generic;

using System.Linq;

using System.Text;

using System.Text.RegularExpressions;

using System.Threading.Tasks;

namespace ConsoleApp11
{
    class Program
    {

        static void Main(string[] args)
        {

            char[] RE = {
            'a','b','0','1','_','.','@'};

            int Count = 0;
            while (Count == 0)
            {

                Console.WriteLine("Your Email for Validation");
                string email = Console.ReadLine();

                if ((email[0] == RE[0] || email[0] == RE[1]) && (email.Contains(RE[6])) && (email[email.Length - 1] != RE[6]) && ((email[email.Length - 1] != RE[4])))
                {

                    Console.WriteLine("Sorry! Your email address is VALID");
                    Console.WriteLine();
                    Console.ReadKey();

                }

                else
                {
                    Console.WriteLine("Entered email address is INVALID");

                }
                Console.WriteLine();
            }

        }


    }

}
