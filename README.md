<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">


   
</head>
<body>

<h1>32-Bit ALU Design in Verilog</h1>

<h2>Introduction</h2>
<p>This project implements a 32-bit Arithmetic Logic Unit (ALU) in Verilog, capable of performing a variety of arithmetic and logical operations. The ALU is a fundamental component in digital systems and forms the core of many processors, handling basic computations required by the CPU.</p>

<h2>Features</h2>
<p>The 32-bit ALU supports the following operations:</p>
<ul>
    <li><strong>Arithmetic Operations:</strong> Addition, Subtraction, Multiplication, Division</li>
    <li><strong>Logical Operations:</strong> AND, OR, XOR, NOR, NOT</li>
    <li><strong>Shift Operations:</strong> Logical Shift Left, Logical Shift Right, Arithmetic Shift Left, Arithmetic Shift Right</li>
    <li><strong>Comparison Operations:</strong> Equality Check (==), Greater Than (>), Less Than (<)</li>
</ul>
<p><strong>Overflow Detection:</strong> The ALU also includes overflow detection for arithmetic operations.</p>

<h2>Files</h2>
<ul>
    <li><strong>design.sv:</strong> Verilog implementation of the 32-bit ALU.</li>
    <li><strong>testbench.sv:</strong> Testbench file for simulating and verifying the ALU's functionality.</li>
    <li><strong>README.md:</strong> Documentation for the project.</li>
</ul>

<h2>How It Works</h2>
<p>
    <strong>1. Input:</strong> Two 32-bit operands are provided as inputs along with control signals to select the desired operation.
</p>
<p>
    <strong>2. Processing:</strong> The ALU performs the operation based on the control signals. Arithmetic, logical, and shift operations are executed within the same ALU module.
</p>
<p>
    <strong>3. Output:</strong> The result of the operation is output as a 32-bit value, with flags for zero, carry, and overflow conditions.
</p>

<h2>Control Signals</h2>
<table>
    <thead>
        <tr>
            <th>Control Signal</th>
            <th>Operation</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>0000</td>
            <td>Addition</td>
        </tr>
        <tr>
            <td>0001</td>
            <td>Subtraction</td>
        </tr>
        <tr>
            <td>0010</td>
            <td>Multiplication</td>
        </tr>
        <tr>
            <td>0011</td>
            <td>Division</td>
        </tr>
        <tr>
            <td>0100</td>
            <td>AND</td>
        </tr>
        <tr>
            <td>0105</td>
            <td>OR</td>
        </tr>
        <tr>
            <td>0110</td>
            <td>XOR</td>
        </tr>
        <tr>
            <td>0111</td>
            <td>NOR</td>
        </tr>
        <tr>
            <td>1000</td>
            <td>NOT</td>
        </tr>
        <tr>
            <td>1001</td>
            <td>Logical Shift Left</td>
        </tr>
        <tr>
            <td>1010</td>
            <td>Logical Shift Right</td>
        </tr>
        <tr>
            <td>1011</td>
            <td>Arithmetic Shift Left</td>
        </tr>
        <tr>
            <td>1100</td>
            <td>Arithmetic Shift Right</td>
        </tr>
        <tr>
            <td>1101</td>
            <td>Equal To</td>
        </tr>
        <tr>
            <td>1110</td>
            <td>Greater Than</td>
        </tr>
        <tr>
            <td>1111</td>
            <td>Less Than</td>
        </tr>
    </tbody>
</table>

<h2>Example Test Cases</h2>
<p>The testbench verifies a variety of ALU operations:</p>
<ul>
    <li><strong>Addition:</strong> 5 + 3 = 8</li>
    <li><strong>Subtraction:</strong> 10 - 4 = 6</li>
    <li><strong>Multiplication:</strong> 7 * 6 = 42</li>
    <li><strong>Logical AND:</strong> 1010 & 1100 = 1000</li>
    <li><strong>Shift Left:</strong> 0010 << 1 = 0100</li>
</ul>
<p>More test cases can be added in the <code>alu_tb.v</code> file.</p>

<h2>Future Enhancements</h2>
<ul>
    <li>Add support for more complex operations (e.g., modulus, exponentiation).</li>
    <li>Optimize the ALU design for speed and area.</li>
    <li>Implement a fully pipelined ALU for better performance.</li>
</ul>

</body>
</html>
