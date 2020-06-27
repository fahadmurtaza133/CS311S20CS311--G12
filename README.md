# CS311S20CS311--G12

// TAKING INPUT IN JAVA FROM USER
// taking a string
		 Scanner myObj = new Scanner(System.in);
		 System.out.println(" Enter the String you want to Print");
		 String a = myObj.nextLine();
		 System.out.println(" Your Name is "+ a);
  // Taking int,float,long,short
		 System.out.println("Enter any integer ");
		 int b = myObj.nextInt();
		 System.out.println("Enter any float number ");
		 float c = myObj.nextFloat();
		 System.out.println("Enter any long number ");
		 double d = myObj.nextLong();
		 
		 System.out.println("Your integer is  "+ b + "Your float is"+ c+ " Your long number is "+ d);


// File Handling in Java

package file.filehandling;
import java.io.File;// Import the File class
import java.io.FileWriter; 
import java.io.IOException;
import java.io.FileNotFoundException;  // Import this class to handle errors
import java.util.Scanner;

public class file {
	
	public static void Filecreation()
	{
		
		// creating new file 
				try
				{
					File myfile = new File("myfile.txt");
					if (myfile.createNewFile())
					{
						System.out.println(" File Created " + myfile.getName());
					}
					else
					{
						System.out.println("File already existed");
					}
				
				
					
				}
				catch (IOException e)
				{ System.out.println("An error occurred.");
			      e.printStackTrace();
			 }
		
		
		
		
		
	}
	
   public static void FileWriter()
   {
	// Write in a created file
		try {	
		FileWriter write = new FileWriter("myfile.txt");
		write.write("HI Fahad, how are you??");
		write.close();
		System.out.println(" Successfully written");
		
		}
		
		catch (IOException f)
		{ 
			System.out.println("Error");
			 f.printStackTrace();
			
		}
   }
   
   public static void FileReader()
   {
	   

		// Read from the file 
		
		try {
			
			File myfile = new File("myfile.txt");
			  Scanner myReader = new Scanner(myfile);
		      while (myReader.hasNextLine())
		      {
		        String data = myReader.nextLine();
		        System.out.println(data);
		       
		
		}
		      myReader.close();
	    } 
		 catch (FileNotFoundException e) {
	      System.out.println("An error occurred.");
	      e.printStackTrace();
	    }
	   
	   
	   
	   
	   
   }
	
	
	public static void main(String[] args)
	 {

		
		Filecreation();
		FileWriter();
		FileReader();
		
 		
		
}
}

		 
		 
