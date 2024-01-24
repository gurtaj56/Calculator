Calculator Explanation: 
This calculator has buttons (1-9), a clear button to reset input, and operations for addition, subtraction, multiplication, division, and percentage. Buttons add digits to the input; clear resets. Multiplication, division, addition, and subtraction set operators and store the 1st operand; percentage calculates based on input. Equals computes results; errors for division by zero or invalid operators. There's an incremental button for '1', considering the input state. However the issue with our calculator is that it can do equations like 12465 * 3, but if that was the other way around the calculator will read it as 3 * 5. 


Buttons: 
The buttons have the same code except for different jButton numbers and values. 
if (jTextField1.getText().isEmpty()) {
            jTextField1.setText(jButton1.getText());
            value1 = 1;
        } else {
            jTextField1.setText(jTextField1.getText() + "" + jButton1.getText()
            ) ;
            value2 = 1;
        } 
// If the text field is empty, sets it to the button's text and updates a corresponding value.
// If not empty, appends the button's text to the existing text in the text field and updates another value.



Clear: 
jTextField1.setText(""); 
//clears the textfield of any numbers


// Handles multiplication button click event.
// If the text field is empty, returns; otherwise, sets value1 and updates the text field with the operator.
Multiplication: 
if(jTextField1.getText().isEmpty())
           return;
        else
            value1 = Integer.parseInt(jTextField1.getText());
            jTextField1.setText( jTextField1.getText() + "" + jButton15.getText() );
            operator = "multiplication";

// Handles division button click event.
// If the text field is empty, returns; otherwise, sets value1 and updates the text field with the operator.
Division: 
if(jTextField1.getText().isEmpty())
           return;
        else
            value1 = Integer.parseInt(jTextField1.getText());
            jTextField1.setText( jTextField1.getText() + "" + jButton16.getText());
            operator = "division";



Addition: 
if (jTextField1.getText().isEmpty()) {
            return;
        } else {
            value1 = Integer.parseInt(jTextField1.getText());
        }
        jTextField1.setText(jTextField1.getText() + "" + jButton2.getText() );
            operator = "plus";
// Handles addition button click event.
// If the text field is empty, returns; otherwise, sets value1 and updates the text field with the operator.


Subtraction: 
if (jTextField1.getText().isEmpty()) {
            return;
        } else {
            value1 = Integer.parseInt(jTextField1.getText());
        }
        jTextField1.setText(jTextField1.getText() + "" + jButton14.getText() );
            operator = "minus";
// Handles subtraction button click event.
// If the text field is empty, returns; otherwise, sets value1 and updates the text field with the operator.


Percentage: 
if(jTextField1.getText().isEmpty())
           return;
        else
            value1 = Integer.parseInt(jTextField1.getText());
            jTextField1.setText( jTextField1.getText() + "" + jButton17.getText() );
            operator = "percentage";
// Handles percentage button click event.
// If the text field is empty, returns; otherwise, sets value1 and updates the text field with the operator.

Equals: 
double answer = 0;

if (operator.equals("plus")) {
    answer = value1 + value2;
} else if (operator.equals("minus")) {
    answer = value1 - value2;
} else if (operator.equals("multiplication")) {
    answer = value1 * value2;
} else if (operator.equals("division")) {
    if (value2 != 0) { 
        answer = value1 / value2;
    } else {
        
        jTextField1.setText("Error: Division by zero");
        return;
    }
} else if (operator.equals("percentage")) {
   
    answer = (value1 * value2) / 100;
} else {
   
    jTextField1.setText("Error: Invalid operator");
    return;
}

String result = Double.toString(answer);
jTextField1.setText(result);
// Calculates the result based on the selected operator and updates the text field.
// Handles division by zero and invalid operator cases.


    }
