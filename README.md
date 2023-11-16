# Operator-Overloading
## Aim:
 To write a C# program to find the volume of a box using operator overloading
 
 ## Algorithm:
 ### Step 1:
 Create a class for operator overloading
### Step 2:
Get inputs for length,breadth and height of the box from the user and then calculate the volume in overloading function
### Step 3:
After that return a new object for the calculated volume
### Step 4:
Then create a new object to store the return object
### Step 5:
After that print the calculated volume 
 
 ## Program:
 ```c#
 using System;

namespace OperOverload
{
    class Program
    {
        int n;
        public Program(int a)
        {
            this.n = a;
            Console.WriteLine("this is a parameterized constructor");
            Console.WriteLine("the value is " + this.n);
        }
        public Program()
        {
            this.n = 100;
            Console.WriteLine("this is a default constructor \n the value is "+ this.n);
        }
        public static bool operator==(Program p1, Program p2)
        {
            return p1.Equals(p2);
        }
        public static bool operator !=(Program p1, Program p2)
        {
            return !p1.Equals(p2);
        }
        static void Main(string[] args)
        {
            Program p1 = new Program(10);
            Program p4 = new Program();

            if (p1 == p4)
            {
                Console.WriteLine("They both are equal");
            }
            else if (p1 != p4)
            {
                Console.WriteLine("They both are different ");
            }
        }
    }
}

 ```
 ## Output:
![image](https://user-images.githubusercontent.com/75234646/198813045-25a2bfa4-de25-408d-bb78-cdec05529d09.png)

 ## Result:
Thus the C# program to find the volume of a box using operator overloading is implemented successfully.
