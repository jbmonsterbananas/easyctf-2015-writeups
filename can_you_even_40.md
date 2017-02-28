# Can You Even??? (40)

## Problem

Use the programming interface to complete this task. You&#39;ll be given a list of numbers.

Input: A list of numbers, separated by commas.

Output: The number of even numbers.

Read the input from a file called&nbsp;`can-you-even.in`&nbsp;that&#39;s in the current working directory, and then write your output to a file called&nbsp;`can-you-even.out`.

## Hint

If you need help, try looking at the Python Tutorial in the Learn section! Perhaps you should try looking into the modulo (%) operator. 

## Write-Up

The main trick about this piece of code is knowing how to use modulus correctly.

```java
import java.io.*;

public class program{

	public static void main(String[] args){
		try{
			BufferedReader reader = new BufferedReader(new FileReader("can-you-even.in"));
			String line = reader.readLine();
			
			String[] nums = line.split(",");
			int sum = 0;
			
   	        for (String s : nums){
				int i = Integer.parseInt(s);	
              	if (i % 2 == 0) //if i is EVEN
					sum++;
            }
			
			PrintStream printer = new PrintStream("can-you-even.out");
			printer.print(sum+"\n");
		} catch(Exception e){
			e.printStackTrace();
		}
	}

}
```

Running this code or equivalent Python code will result in the flag.

flag = `easyctf{?v=8ruJBKFrRCk}`

BTW, check out this cool link I found, [www.youtube.com/watch?v=8ruJBKFrRCk](http://www.youtube.com/watch?v=8ruJBKFrRCk)
