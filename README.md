using System;

class Program
{
    static void Main() {
     
            
        Console.WriteLine("Employee Time Keeping System");
            Console.WriteLine($"Today's Date:  {DateTime.Today.ToShortDateString()}");

            Console.Write("To log your time-in enter your employee id:");
            string employeeId = Console.ReadLine();

          
            TimeSpan timeIn = new TimeSpan(8,0,0);
            Console.WriteLine($"Your login time is recorded: {timeIn}");
            

            Console.WriteLine("*********************************");
            Console.Write("To log your time-out enter your employee id:");
            employeeId = Console.ReadLine();

            TimeSpan timeOut = new TimeSpan(16, 0, 0);
            Console.WriteLine($"Your logout time is recorded: {timeOut}");

            TimeSpan lunchBreakDuration = new TimeSpan(1, 0, 0);
            TimeSpan totalHours = (timeOut - timeIn) - lunchBreakDuration;

            Console.WriteLine($"Yout total hours worked is: {totalHours}");
            
            
           

          Console.WriteLine("You are Undertime");
           
            
    }
}


