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

### Day 11
• Learned to convert a string number into other data types by using a method;

ex: ``` int number = Integer.parseInt(numberAsString); ```

• I've done a 'number to words' converter. This challenge was a bit more difficult but I managed to get the job done :sunglasses: 

```
public class Main {

    public static void main(String[] args) {
        numberToWords(120100);

    }

    public static void printNumber(int number) {
        while (number != 0) {
            for (int i = 0; i <= 9; i++) {
                if (i == number % 10) {
                    switch (i) {
                        case 0:
                            System.out.println("Zero");
                            break;
                        case 1:
                            System.out.println("One");
                            break;
                        case 2:
                            System.out.println("Two");
                            break;
                        case 3:
                            System.out.println("Three");
                            break;
                        case 4:
                            System.out.println("Four");
                            break;
                        case 5:
                            System.out.println("Five");
                            break;
                        case 6:
                            System.out.println("Six");
                            break;
                        case 7:
                            System.out.println("Seven");
                            break;
                        case 8:
                            System.out.println("Eight");
                            break;
                        case 9:
                            System.out.println("Nine");
                            break;
                    }
                }
            }

            number /= 10;
        }
    }

    public static int reverse(int number) {
        int reverseNumber = 0;

        while (number != 0) {
            reverseNumber = (reverseNumber * 10) + (number % 10);
            number /= 10;
        }

        return reverseNumber;
    }

    public static int getDigitCount(int number) {
        if(number < 0) {
            return -1;
        }

        int count = 0;

        while (number != 0) {
            count++;
            number /= 10;
        }
        if (count == 0) {
            return 1;
        } else {
            return count;
        }
    }

    public static void numberToWords(int number) {
        if (number < 0) {
            System.out.println("Invalid Value");
        } else if (number == 0) {
            System.out.println("Zero");
        } else {
            int numberDigits = getDigitCount(number);
            int numberReverse = reverse(number);
            int numberDigitsRevers = getDigitCount(numberReverse);

            if (numberDigits == numberDigitsRevers) {
                printNumber(numberReverse);

            } else {
                int difDigits = numberDigits - numberDigitsRevers;
                printNumber(numberReverse);

                for (int i = 1; i <= difDigits; i++) {
                    System.out.println("Zero");
                }
            }
        }
    }
}


```
```
One
Two
Zero
One
Zero
Zero

Process finished with exit code 0
```

### Day 12
• I revised everything I learned in Java Masterclass course;

• Solved 2 exercises;

• It's getting harder :arrow_right: challenge accepted :smirk_cat:

### Day 13
• Completed 1 exercise;

• Learned how to read user's input.

### Day 14
• Completed one more challenge and finished section 5 (Control Flow Statements).

### Day 15
• Started section 6 in Java Masterclass course (OOP Part 1 - Classes, Constructors and Inheritance);

• Understood the basics of classes and objects + played around with getters and setters :laughing:

• It sounds interesting to me!! Can't wait to gain more knowledge :octocat:

### Day 16
• I've read more about classes and objects in Java for Dummies book and in Oracle's Java Documentation;

• Learned how to use class constructors and how to set different values or default values to the fields of an object  :wrench:

• Completed one challenge.

### Day 17
• Revised some concepts by reading Oracle's Java Doc;

• Completed one lesson about inheritance;

• Learned how to override methods.

### Day 18
• Completed one more lesson about inheritance;

• Learned what ```super``` keyword does.

### Day 19
• Learned about references to objects and understood how they work;

• I've read more about ```this()```, ```super()``` methods and constructor chaining :nut_and_bolt:

### Day 20
• Recaped method overloading and overriding;

• Learned the difference between static and instance methods, respectively between static and instance variables.

### Day 21
• Finished section 6 in Java Masterclass course (OOP Part 1 - Classes, Constructors and Inheritance).

### Day 22
• Recaped all Java concepts that I've learned.

### Day 23
• Started section 7 in Java Masterclass course (OOP Part 2 - Composition, Encapsulation and Polymorphism);

• Completed 1 lesson about Composition  :smirk_cat:

### Day 24
• Completed 1 more lesson about Composition and 1 challenge;

• Understood the difference between 'Is-a' and 'Has-a' relationships.

• I'm really curious about Codewars. Feeling like I need more challenges to strenghten my knowledge.. I'll go for it after I learn arrays :bowtie:

### Day 25
• Learned what encapsulation is;

• I was using it before knowing what it is.

### Day 26
• Completed 1 encapsulation challenge :smirk_cat:

### Day 27
• Completed 1 lesson about the concept of polymorphism. 

### Day 28
• Completed 1 polymorphism challenge.

### Day 29
• Started the last challenge of OOP section in Java Masterclass course.

### Day 30
• Finished the challenge and the section 7 in the course (OOP Part 2 - Composition, Encapsulation and Polymorphism).

### Day 31
• Missed this day :confused:

### Day 32
• Did the last challenge again in order to get a better understanding of the concepts.

### Day 33
• Recaped all the things that I've learned;

• Started section 8 (Arrays, Java inbuilt Lists, Autoboxing and Unboxing);

• Completed a lesson about arrays.

### Day 34
• Read about arrays in Oracle's Java docs;

• Completed 1 challenge, had to get an array from the console and sort it;

• Used some useful in built methods.

### Day 35
• Recaped arrays.

### Day 36
• Completed a lesson about differences between reference types and value types;

• Solved an exercise.

### Day 37
• Solved an exercise;

• Learned about Array Lists.

### Day 38
• Used some useful in built functions.

• Made a mini grocery list application, it was fun :bowtie:

• Here are the commands you can use in the app:
```
Press 
	 0 - To print choice options.
	 1 - To print the list of grocery items.
	 2 - To add an item to the list.
	 3 - To modify an item in the list.
	 4 - To remove an item from the list.
	 5 - To search for an item in the list.
	 6 - To quit the application.
Enter your choice 
```
### Day 39
• Did the last challenge from scratch again in order to consolidade my knowledge :smirk_cat:

### Day 40
• Started a mini 'mobile phone' app. 

### Day 41
• Finished the challenge;

• Used a factory method.

### Day 42
• Did the challenge once again in order to get a better understanding of array lists :innocent:

### Day 43
• Learned about the concept of auto boxing and unboxing :truck:

• Merry Christmas!! :santa: :christmas_tree: :gift:

### Day 44
• Built a mini banking app.

### Day 45
• Learned about linked lists. They seem a bit complicated.

### Day 46
• Learned how to use list iterators and how to control the pointing direction in a linked list :arrows_counterclockwise:

• Built a mini app.

### Day 47
• Built a mini song app bt using linked lists.

### Day 48
• Finished section 8 (Arrays, Java inbuilt Lists, Autoboxing and Unboxing).

### Day 49
• Started section 9 (Inner and Abstract Classes & Interfaces);

• Completed 2 lessons about interfaces.

### Day 50
• Completed a challenge;
