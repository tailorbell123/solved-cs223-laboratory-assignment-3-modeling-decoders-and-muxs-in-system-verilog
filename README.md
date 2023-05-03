Download Link: https://assignmentchef.com/product/solved-cs223-laboratory-assignment-3-modeling-decoders-and-muxs-in-system-verilog
<br>






<h1>Preliminary Report (30 points)</h1>

Today’s lab needs considerable advance preparation. These advance designs and SystemVerilog models should be prepared in advance, and assembled neatly into a Preliminary Report with a cover page and pages for the SystemVerilog codes. Each page should have a proper heading. The report should be uploaded on Moodle as a pdf file before the start of the lab. The content of the report will be as follows:

<ol>

 <li>A cover page including: course code, course name and section, the number of the lab, your name-surname, student ID, date.</li>

 <li>Behavioral SystemVerilog module for 2-to-4 decoder and a testbench for it.</li>

 <li>Behavioral SystemVerilog module for 4-to-1 multiplexer.</li>

 <li>Schematic (block diagram) and structural System Verilog module of 8-to-1 MUX by using two 4-to-1 MUX modules, two AND gates, an INVERTER, and an OR gate. Prepare a test bench for it.</li>

 <li>Schematic (block diagram)          and      SystemVerilog            module            for F(A,B,C,D)=∑(0,1,3,4,7,8,10,11,15) function, using one (not two) 8-to-1 multiplexer and an inverter.</li>

</ol>

You can refer to the slides of chapter 4 of your textbook while preparing your modules and test benches. Don’t forget that you have to hand in your reports at the start of the labs and penalties may apply if you fail to do so!

<strong> </strong>

<strong> </strong>




<strong> </strong>

<h1>Part A: Decoders (25 points)</h1>

Decoders are widely used in digital design, as a building block. Although they themselves can be built with logic gates, their function is often described (and modeled in System Verilog) rather than their structure. As you will see, decoders can be composed into larger decoders.

A 2-to-4 decoder decodes a 2-bit input binary number by setting exactly one of the decoder’s 4 outputs to 1. Unless it has an enable signal, one and only one output of a decoder will ever be 1 at the same time, corresponding to the current value of the inputs. With an enable signal, it is possible to make all the outputs be 0, when the decoder is disabled. When enabled, it behaves as described above. Decoder outputs are mutually exclusive, and in fact are the minterms of the inputs.

 <em>Create a new Xilinx Vivado Project to do a), b), c) and d). Use appropriate names for files and folders, keeping the project in a directory where you can find it later and erase it (at the end of lab).</em>

<ol>

 <li><u>Write code</u>: Give the System Verilog code which models a 2-to-4 decoder in behavioral style. (This means modeling with Boolean equations, using continuous assignment statements.)</li>

 <li><u>Simulate it</u>: Using the System Verilog testbench code, verify in simulation that your 2-to-4 decoder with enable is working correctly. (Be sure to compare the order of the ports in your module with the order of the ports in the instantiation of your decoder in the testbench, to make sure they match 1-to-1.)</li>

 <li><u>Make FPGA project</u>: Now, follow the Xilinx design flow to synthesize, create programming file, and download your 2-to-4 decoder to your BASYS-3 FPGA board.</li>

 <li><u>Test it</u>: Using the switches and LEDs on BASYS-3 that you have assigned now, test your decoder. When you are convinced that it works correctly, show the physical implementation results to the TA. Be prepared to answer questions that you may be asked.</li>

</ol>

<strong> </strong>

<h1>Part B: Multiplexers and Boolean function implementation (45points)</h1>

A multiplexer (“MUX” for short) is another higher-level building block, used widely in digital design. A M-to-1 multiplexer has M data inputs and 1 data output, and allows only one input to pass through to the output. A set of select inputs determines which input to pass through. MUXs can be composed into larger MUXs, as you will see in this part of the lab.

<ol>

 <li><u>Write code</u>: Give dataflow System Verilog module for a 4-to-1 multiplexer.</li>

 <li><u>Simulate it</u>: Simulate your 4-to-1 multiplexer and show it to your TA.</li>

 <li><u>Write code</u>: Write structural System Verilog code for an 8-to-1 multiplexer using two 4-to-1 multiplexers, two AND gates, an OR gate and an inverter.</li>

 <li><u>Simulate it</u>: Simulate 8-to-1 multiplexer and show it to your TA.</li>

 <li><u>Test it</u>: Set up the circuit you designed for F(A,B,C,D)=∑(0,1,3,4,7,8,10,11,15) in preliminary work in a new module, using a single 8-to-1 multiplexer. Using inverses of signals is allowed. Test your circuit using switches as input and a LED as output. Show your circuit to TA. Be prepared to answer questions that you may be asked.</li>

</ol>




<h1>Submit your code for MOSS similarity testing</h1>

Finally, when you are done and before leaving the lab, you need to copy all the SystemVerilog codes you wrote to a txt file named <em><u>StudentID_name.txt</u></em> and upload it to Moodle. If you have multiple files, just copy and paste them in order, one after another inside text file. Even if you didn’t finish or didn’t get the SystemVerilog part working, you must submit your code to the Moodle for similarity checking. Your codes will be compared against all the other codes in all sections of the class, by the MOSS program, to determine how similar it is (as indication of plagiarism). So be sure that the code you submit is the code that you actually wrote yourself!








