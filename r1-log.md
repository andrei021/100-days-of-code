# #100DaysOfCode Log - Round 1 - Andrei Mihai

The log of my #100DaysOfCode challenge. Started on [November 12, Monday, 2018].

## Log

### Day 1 
Completed 3 lessons in Tim's Java Masterclass on Udemy. It was my first encounter with Java methods and I got it pretty easily.

### Day 2
```
public class Main {

    public static void main(String[] args) {
        printMegaBytesAndKiloBytes(2050);
    }

    public static void printMegaBytesAndKiloBytes(int kiloBytes) {
        int megaBytes = kiloBytes / 1024;
        int remainingKiloBytes = kiloBytes % 1024;

        if (kiloBytes < 0) {
            System.out.println("Invalid Value");
        } else {
            System.out.println(kiloBytes + " KB = " + megaBytes + " MB and " + remainingKiloBytes + " KB");
        }
    }
}

```



