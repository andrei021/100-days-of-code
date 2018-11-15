# #100DaysOfCode Log - Round 1 - Andrei Mihai

The log of my #100DaysOfCode challenge. Started on [November 12, Monday, 2018].

## Log

### Day 1 
Completed 3 lessons in Tim's Java Masterclass on Udemy. It was my first encounter with Java methods and I got it pretty easily.

### Day 2
I've read more about Java methods in Java For Dummies book, installed and got familiarized with DiffMerge tool and successfully done a MegaBytes Converter exercise on Udemy. Felt excited :)

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
```
2050 KB = 2 MB and 2 KB

Process finished with exit code 0
```

### Day 3
Completed 5 more exercises in Java Masterclass course on Udemy. I really enjoy using methods :sunglasses:

### Day 4
• Took one lesson on Udemy about method overloading;

• I also did a "inches to centimeters" converter by using 2 methods: one transforms the inches to feet and remaining inches and the other one takes the previous result and converts it to centimeters. 

I know I could have done it directly from inches to centimeters but that's not what the exercise asked. It 'forced' me to call a method within another method and that obviously helps me getting a better understanding of methods.

Coding is fun! :stuck_out_tongue_closed_eyes:

```
public class Main {

    public static void main(String[] args) {
        calcFeetAndInchesToCentimeters(50);

    }

    public static double calcFeetAndInchesToCentimeters(double feet, double inches) {
        if ((feet >= 0) && ((inches >= 0) && (inches <= 12))) {
            double cm = inches * 2.54 + feet * 12 * 2.54;
            System.out.println(feet + " ft and " + inches + " in = " + cm + " cm");
            return 1;
        }

        return -1;
    }

    public static double calcFeetAndInchesToCentimeters(double inches) {
        if (inches >= 0) {
            double feet = (int) (inches / 12);
            double rInches = inches % 12;

            System.out.println(inches + " in = " + feet + " ft and " + rInches + " in");
            return calcFeetAndInchesToCentimeters(feet, rInches);
        }

        System.out.println("Invalid value");
        return -1;
    }

}
```
```
50.0 in = 4.0 ft and 2.0 in
4.0 ft and 2.0 in = 127.0 cm

Process finished with exit code 0
```







