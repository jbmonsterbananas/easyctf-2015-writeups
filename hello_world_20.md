# Hello World! (20)

## Problem

Use the programming interface to complete this task. Print the line `Hello, EasyCTF!` to a file called `hello-world.out`. For this problem and for future problems,&nbsp;**make sure your program ends with a newline**. Good luck!

## Hint

If you're really stuck, contact one of the mods on the [chat](https://www.easyctf.com/chat), or check out our [video tutorial](https://www.youtube.com/watch?v=GP1ZfzRSclQ)!

## Write-Up

Hello, EasyCTF!

```java
import java.io.*;

public class program{
	
	public static void main(String[] args){
		try{
			PrintStream p = new PrintStream("hello-world.out");
			p.print("Hello, EasyCTF!\n");
		} catch(Exception e){
			e.printStackTrace();
		}
	}
	
}
```

flag = `easyctf{welc0me_two_easyCtf}`
