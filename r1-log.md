# #100DaysOfCode - Round 1 - Learning Java - Andrei Mihai 

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

• I also did a 'inches to centimeters' converter by using 2 methods: one transforms the inches to feet and remaining inches and the other one takes the previous result and converts it to centimeters. 

I know I could have done it directly from inches to centimeters but that's not what the exercise asked. It 'forced' me to call a method within another method (not main :laughing:), which obviously helps me getting a better understanding of the methods.

Coding is fun! :stuck_out_tongue_closed_eyes:

```
public class Main {

    public static void main(String[] args) {
        calcFeetAndInchesToCentimeters(122.6);

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
122.6 in = 10.0 ft and 2.5999999999999943 in
10.0 ft and 2.5999999999999943 in = 311.404 cm

Process finished with exit code 0
```

### Day 5
I've done a 'seconds to hours, minutes and seconds' converter and used a constant for the first time.

### Day 6
I've done the last 4 exercises of section 4 (Expressions, Statements, Code blocks, Methods and more) in Java Masterclass course.

### Day 7
• I've started section 5 (Control flow statements) and learned to use the switch statement;

• Undestood what break statement does;

• I have also done 2 exercises :aries: 

### Day 8
Learned the for statement and completed 2 exercises.

### Day 9
• Learned the while and do-while statements;

• Completed 1 exercise;

• Understood how continue statement works in a loop.

### Day 10
• Easily solved 8 more exercises by using loops;

• I got the concepts pretty well and I'm looking forward to get more challenges done :smirk_cat:






