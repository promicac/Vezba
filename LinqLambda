using System;

using System.Collections.Generic;

using System.Linq;



			



class Student { 
      
    // properties rollNo and name 
    public int rollNo 
    { 
        get; 
        set; 
    } 
      
    public string name 
    { 
        get; 
        set; 
    } 
} 



public class Program
{
	public static void Main()
	{
		
		
		
		List<Student> details = new List<Student>() { 
            new Student{ rollNo = 1, name = "Liza" }, 
                new Student{ rollNo = 2, name = "Stewart" }, 
                new Student{ rollNo = 3, name = "Tina" }, 
                new Student{ rollNo = 4, name = "Stefani" }, 
                new Student { rollNo = 5, name = "Trish" } 
        }; 
		
		
		
		var uredjen = details.OrderBy(x=>x.name);
		
		
		 foreach(var value in uredjen) 
        { 
            Console.WriteLine(value.rollNo + " " + value.name); 
        } 
    } 
		
		
		
	}
