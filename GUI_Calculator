//Name of Program: Simple Calculator (using +, -, /, * operators)
//Name: Lee Sebin (21900513)
//Develop Date: 2020-05-14


//import these to use GUI
import java.awt.event.*; 
import javax.swing.*; 
import java.awt.*;

class Calculator extends JFrame implements ActionListener { 
  
 static JFrame f; // Create a frame

 static JTextField t; // Create calculation screen
 
 static JPanel p = new JPanel(); // create a panel
 String n1, op, n2; // n1 & n2: numbers and op: operands

 // Constructor that defaults all numbers and operands
 Calculator() 
 { 
     n1 = op = n2 = ""; 
 }
 
 public static void Screen_detail(Calculator c) {
	 f = new JFrame("Simple Calculator"); //frame's name
	  
	// Set the details of calculation screen
     t = new JTextField(19);
     t.setBackground(new Color(194, 204, 196));
     t.setEditable(false); // Prevents the calculation screen from being edited.
	 
 }
 
 public static void panel_detail(Calculator c) {
	 p.setBackground(new Color(134, 179, 0)); // background color (light green)      
	 f.setSize(390, 220); // size of panel
	 f.setResizable(false);
	 f.show();
 }
 
 
 public static void add_elements(Calculator c) {
	 
	 Screen_detail(c);
	 
	 
	// define number buttons and some operators
     JButton b0, b1, b2, b3, b4, b5, b6, b7, b8, b9, add, sub, div, mul, dec, clear, res; 

     // create number buttons (0 to 9)
     b0 = new JButton("0"); 
     b1 = new JButton("1"); 
     b2 = new JButton("2"); 
     b3 = new JButton("3"); 
     b4 = new JButton("4"); 
     b5 = new JButton("5"); 
     b6 = new JButton("6"); 
     b7 = new JButton("7"); 
     b8 = new JButton("8"); 
     b9 = new JButton("9"); 

     
     // create operator buttons 
     add = new JButton("+"); 
     sub = new JButton("-"); 
     div = new JButton("/"); 
     mul = new JButton("*");  

     // create others
     res = new JButton("="); 
     dec = new JButton("."); //decimal point
     clear = new JButton("C"); //clear

     
     // add action listeners 
     mul.addActionListener(c); 
     div.addActionListener(c); 
     sub.addActionListener(c); 
     add.addActionListener(c); 
     b9.addActionListener(c); 
     b8.addActionListener(c); 
     b7.addActionListener(c); 
     b6.addActionListener(c); 
     b5.addActionListener(c); 
     b4.addActionListener(c); 
     b3.addActionListener(c); 
     b2.addActionListener(c); 
     b1.addActionListener(c); 
     b0.addActionListener(c); 
     dec.addActionListener(c); 
     clear.addActionListener(c); 
     res.addActionListener(c);
     
     
     // add elements to panel -> show this buttons on the calculator window
     // Write in the order to appear on the calculator
     p.add(t);
     p.add(clear);
     p.add(b7);
     p.add(b8);
     p.add(b9); 
     p.add(div);
     p.add(b4);
     p.add(b5); 
     p.add(b6);
     p.add(mul);
     p.add(b1); 
     p.add(b2); 
     p.add(b3); 
     p.add(sub); 
     p.add(b0);     
     p.add(dec);         
     p.add(res);
     p.add(add);
     
     f.add(p); // add panel to frame
    
	 
 }
 

 // main function 
 public static void main(String args[])
 { 

     try { //Exception handling syntax in case the path cannot be found
         UIManager.setLookAndFeel(UIManager.getSystemLookAndFeelClassName()); 
     } 
     catch (Exception e) {
         System.err.println(e.getMessage()); 
     } 

     Calculator c = new Calculator();
     
     add_elements(c);
     
     panel_detail(c);
 }
 
 
 //method to calculate
 public void actionPerformed(ActionEvent e) // Called and executed when ActionEvent occurs.
 { 
     String s = e.getActionCommand(); // Classification of button values ​​pressed by the user

     // if user press number(0 to 9) or decimal number(.) button
     if ((s.charAt(0) >= '0' && s.charAt(0) <= '9') || s.charAt(0) == '.') {  
         if (!op.equals("")) // if there's no operator
             n2 = n2 + s; 
         else
             n1 = n1 + s; 
         
         t.setText(n1 + op + n2); // set the value of text
     }
     
     // else if user press button 'C' -> clear
     else if (s.charAt(0) == 'C') {  
         n1 = op = n2 = "";  
         t.setText(n1 + op + n2); 
     } 
     
     // else if user press button '=' -> Value is calculated.
     else if (s.charAt(0) == '=') { 

         double result; // value for store result

         // Four arithmetic operations (+, -, /, *)
         if (op.equals("+"))
             result = (Double.parseDouble(n1) + Double.parseDouble(n2)); 
         else if (op.equals("-")) 
             result = (Double.parseDouble(n1) - Double.parseDouble(n2)); 
         else if (op.equals("/")) 
             result = (Double.parseDouble(n1) / Double.parseDouble(n2)); 
         else
             result = (Double.parseDouble(n1) * Double.parseDouble(n2)); 

         t.setText(n1 + op + n2 + "=" + result); 

         n1 = Double.toString(result);  
         op = n2 = ""; 
     } 
     
     else { 
         // if there was no operand 
         if (op.equals("") || n2.equals("")) 
             op = s;
         
         // else evaluate result
         else { 
             double result; 

             if (op.equals("+")) 
                 result = (Double.parseDouble(n1) + Double.parseDouble(n2)); 
             else if (op.equals("-")) 
                 result = (Double.parseDouble(n1) - Double.parseDouble(n2)); 
             else if (op.equals("/")) 
                 result = (Double.parseDouble(n1) / Double.parseDouble(n2)); 
             else
                 result = (Double.parseDouble(n1) * Double.parseDouble(n2)); 

             n1 = Double.toString(result); 

             op = s; 
             n2 = ""; 
         } 

         t.setText(n1 + op + n2); 
     } 
 } 
}
