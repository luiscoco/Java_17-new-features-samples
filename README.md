# Java 17 new features samples

## 1. New macOS Rendering Pipeline (JEP 382)

https://openjdk.org/jeps/382

**Java 17 language specification: https://docs.oracle.com/javase/specs/jls/se17/html/index.html**

While the **New macOS Rendering Pipeline (JEP 382) in Java 17** is more about the underlying rendering mechanism that Java uses on macOS rather than a feature that developers interact with directly, I provide you

with a Java application code sample that demonstrates using Java Swing

This GUI application will benefit from the improved rendering pipeline on macOS without needing any code specific to JEP 382

The rendering improvements are under-the-hood and automatic for applications running on macOS with Java 17 or later

Let's create a simple Java Swing application that creates a basic user interface with some graphical elements

This example will run on any platform, but when run on macOS with Java 17 or later, it will automatically utilize the new Metal-based rendering pipeline

```java
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import javax.swing.SwingUtilities;

public class MetalRenderingDemo {

    private static void createAndShowGUI() {
        // Create the window (JFrame) and set its title and default close operation
        JFrame frame = new JFrame("Java 17 Metal Rendering Demo");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Create a panel (JPanel) to hold our components
        JPanel panel = new JPanel();

        // Add a label (JLabel) to the panel
        JLabel label = new JLabel("Hello, macOS Metal Rendering!");
        panel.add(label);

        // Add a button (JButton) to the panel
        JButton button = new JButton("Click Me!");
        button.addActionListener(e -> System.out.println("Button was clicked!"));
        panel.add(button);

        // Add the panel to the frame
        frame.getContentPane().add(panel);

        // Pack the frame (size it to fit the preferred sizes of its components)
        frame.pack();

        // Center the frame on the screen and make it visible
        frame.setLocationRelativeTo(null);
        frame.setVisible(true);
    }

    public static void main(String[] args) {
        // Ensure the GUI is created and updated on the Event Dispatch Thread
        SwingUtilities.invokeLater(MetalRenderingDemo::createAndShowGUI);
    }
}
```

This code demonstrates a basic Java Swing application that includes a window containing a label and a button

When run on macOS with Java 17 or later, this application will benefit from the new Metal-based rendering pipeline, enjoying smoother and more efficient rendering

On other platforms or older versions of Java, it will fall back to the platform's default rendering pipeline

**To run this example**:

Ensure you have Java 17 or later installed on your macOS system

Save the code to a file named MetalRenderingDemo.java

Compile the code using the Java compiler: javac MetalRenderingDemo.java

Run the compiled class: java MetalRenderingDemo

This is a straightforward example, but the performance and efficiency improvements with the new rendering pipeline will be more noticeable in more complex and graphically intensive Swing applications

## 2. macOS/AArch64 Port (JEP 391)

https://openjdk.org/jeps/391

## 3. Strongly Encapsulate JDK Internals (JEP 403)

https://openjdk.org/jeps/403

## 4. Restore Always-Strict Floating-Point Semantics (JEP 306)

https://openjdk.org/jeps/306

## 5. Pattern Matching for switch 1. Preview (JEP 406)

https://openjdk.org/jeps/406

## 6. Sealed Classes (JEP 409)

https://openjdk.org/jeps/409

## 7. Enhanced Pseudo-Random Number Generators (JEP 356)

https://openjdk.org/jeps/356

## 8. Deprecate the Applet API for Removal (JEP 398)

https://openjdk.org/jeps/398

## 9. Remove RMI Activation (JEP 407)

https://openjdk.org/jeps/407

## 10. Deprecate the Security Manager for Removal (JEP 411)

https://openjdk.org/jeps/411

## 11. Foreign Function & Memory API 1 (JEP 412)

https://openjdk.org/jeps/412

## 12. Vector API 2 (JEP 414)

https://openjdk.org/jeps/414

## 13. Remove the Experimental AOT and JIT Compiler (JEP 410)

https://openjdk.org/jeps/410
