# Robust Shape Design for Secure Systems

In the context of cybersecurity, having a solid understanding of object-oriented programming (OOP) principles, like encapsulation and constructor use, is crucial. These principles not only help in building maintainable and modular systems but also in creating secure and efficient software. This project demonstrates how to design a **Rectangle** class using Java, which incorporates OOP concepts to model a real-world object.

# Intuition

The goal of this project is to model a rectangle using Java, providing the ability to calculate and retrieve its area, perimeter, and other essential attributes. A rectangle can be represented by two main properties: width and height. By using constructors and getter methods, we allow users to create rectangles with default values or user-defined dimensions, and then calculate and display important properties like the area and perimeter.

# Approach

1. **Create a Rectangle class**: The class has two private attributes: `width` and `height`. These attributes are initialized using constructors.

2. **Define Constructors**:
   - A **default constructor** initializes the rectangle with default values (width = 1.00 and height = 1.00).
   - A **parameterized constructor** allows the user to input specific values for width and height.

3. **Get Methods**: The `getWidth` and `getHeight` methods allow access to the rectangle's width and height.

4. **Utility Methods**:
   - `getArea()`: Calculates the area of the rectangle (width * height).
   - `getPerimeter()`: Calculates the perimeter of the rectangle (2 * (width + height)).
   - `printRectangle(String objectName)`: Prints a formatted description of the rectangle with a specified name.

5. **Test Program**: A main program allows the user to enter values for a rectangle, and displays the rectangle’s properties such as width, height, area, and perimeter.

# Complexity

- **Time Complexity**: $$O(1)$$

  All operations in the `Rectangle` class (getter methods, area, perimeter calculations) are constant time operations because they involve simple arithmetic and attribute access.

- **Space Complexity**: $$O(1)$$

  The space complexity is constant, as we only use a fixed amount of memory to store the width, height, and computed values (area, perimeter), regardless of input size.

# Code
```java
public class Rectangle {
    private double width;
    private double height;

    // Default constructor
    public Rectangle() {
        width = 1.00;
        height = 1.00;
    }

    // Constructor with parameters
    public Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    // Getter methods
    public double getWidth() {
        return width;
    }

    public double getHeight() {
        return height;
    }

    // Method to calculate the area
    public double getArea() {
        return width * height;
    }

    // Method to calculate the perimeter
    public double getPerimeter() {
        return 2 * (width + height);
    }

    // Print the rectangle's description
    public void printRectangle(String objectName) {
        System.out.println("Rectangle " + objectName + " is " + width + " units wide and " + height + " units high.");
    }
}

import java.util.Scanner;

public class TestRectangle {
    public static void main(String[] args) {
        // Create default rectangle (myRectangle)
        Rectangle myRectangle = new Rectangle();

        // Create the user rectangle (yourRectangle)
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter width for your rectangle: ");
        double width = scanner.nextDouble();
        System.out.print("Enter height for your rectangle: ");
        double height = scanner.nextDouble();
        Rectangle yourRectangle = new Rectangle(width, height);

        // Print myRectangle
        System.out.println("Test data: myRectangle:");
        System.out.println("------------");
        System.out.println("Width: " + myRectangle.getWidth());
        System.out.println("Height: " + myRectangle.getHeight());
        System.out.println("Area: " + myRectangle.getArea());
        System.out.println("Perimeter: " + myRectangle.getPerimeter());
        myRectangle.printRectangle("myRectangle");

        // Print  yourRectangle
        System.out.println("\nyourRectangle:");
        System.out.println("--------------");
        System.out.println("Width: " + yourRectangle.getWidth());
        System.out.println("Height: " + yourRectangle.getHeight());
        System.out.println("Area: " + yourRectangle.getArea());
        System.out.println("Perimeter: " + yourRectangle.getPerimeter());
        yourRectangle.printRectangle("yourRectangle");

        // Close the scanner
        scanner.close();
    }
}
```
# Conclusion

This project demonstrates how to model a rectangle object using Java, and showcases the use of object-oriented programming principles such as constructors, getter methods, and encapsulation. In the context of cybersecurity, understanding these basic programming concepts is essential for building secure, maintainable systems and automating processes that can contribute to enhanced data security and system efficiency.

