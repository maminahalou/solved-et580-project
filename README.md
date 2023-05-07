Download Link: https://assignmentchef.com/product/solved-et580-project
<br>



<strong>Makefile </strong>

Submit an edited <em>makefile</em> which runs the <em>phase</em> file you wish to have graded.




<strong>Window</strong>s

<em>Select/Highlight</em> all files in your project. <em>Right click</em>, <em>Send To</em>, <em>Compressed (zipped) Folder</em>.




<strong>OSX</strong>

<em>Select/Highlight</em> all files in your project. <em>Right click</em>, <em>Compress X Items</em>.

<h1>Blackboard</h1>

<ol>

 <li>Rename the zip file <em>zip</em> such as <em>John_Smith.zip.</em></li>

 <li>Open the <em>Project</em> folder in Course Documents.</li>

 <li>Click <em>Project Assignment</em></li>

 <li>Drag your named .zip file into the <em>upload</em> Click <em>Submit</em>.</li>

</ol>

<strong> </strong>

<h1>REQUIRED FILES FOR SUBMISSION</h1>




<table width="504">

 <tbody>

  <tr>

   <td width="96">makefile</td>

   <td width="408">(edit to automatically run the <em>Phase_#.cpp</em> you choose)</td>

  </tr>

  <tr>

   <td width="96">MyArray.h</td>

   <td width="408">(modified version of Template Homework, <em>MyArray.cpp</em> not required)</td>

  </tr>

 </tbody>

</table>

Airline.h

Airline.cpp

Airport.h

Airport.cpp

Flight.h

Flight.cpp

Passenger.h

Passenger.cpp

<table width="517">

 <tbody>

  <tr>

   <td width="96">Person.hPilot.hPilot.cpp</td>

   <td width="421">(abstract class, <em>Person.cpp</em> not required)</td>

  </tr>

  <tr>

   <td width="96">Phase_1.cpp</td>

   <td width="421">(do not edit, used to test project skeleton)</td>

  </tr>

  <tr>

   <td width="96">Phase_2.cpp</td>

   <td width="421">(do not edit, used to test default constructors and output)</td>

  </tr>

  <tr>

   <td width="96">Phase_3.cpp</td>

   <td width="421">(do not edit, used to test accessors and mutators)</td>

  </tr>

  <tr>

   <td width="96">Phase_4.cpp</td>

   <td width="421">(do not edit, used to test <em>MyArray </em>data members and related functions)</td>

  </tr>

  <tr>

   <td width="96">Phase_5.cpp</td>

   <td width="421">(must edit, used to build a project interface)</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h1>DOWNLOADABLE FILES</h1>




makefile.            (edit to automatically run the <em>Phase_#.cpp</em> you choose)

<table width="517">

 <tbody>

  <tr>

   <td width="96">Phase_1.cpp</td>

   <td width="421">(do not edit, used to test project skeleton)</td>

  </tr>

  <tr>

   <td width="96">Phase_2.cpp</td>

   <td width="421">(do not edit, used to test default constructors and output)</td>

  </tr>

  <tr>

   <td width="96">Phase_3.cpp</td>

   <td width="421">(do not edit, used to test accessors and mutators)</td>

  </tr>

  <tr>

   <td width="96">Phase_4.cpp</td>

   <td width="421">(do not edit, used to test <em>MyArray </em>data members and related functions)</td>

  </tr>

  <tr>

   <td width="96">Phase_5.cpp</td>

   <td width="421">(must edit, used to build a project interface)</td>

  </tr>

 </tbody>

</table>

<strong>CONSOLE/MAKEFILE COMMANDS  </strong>

<strong> </strong>

<h1>OSX                             Windows</h1>

<table width="584">

 <tbody>

  <tr>

   <td width="96">make</td>

   <td width="48"> </td>

   <td width="144">mingw32-make</td>

   <td width="48"> </td>

   <td width="248">run the makefile</td>

  </tr>

  <tr>

   <td width="96">make clean</td>

   <td width="48"> </td>

   <td width="144">mingw32-make clean</td>

   <td width="48"> </td>

   <td width="248">run the clean portion of the makefile</td>

  </tr>

  <tr>

   <td width="96">clear</td>

   <td width="48"> </td>

   <td width="144">cls</td>

   <td width="48"> </td>

   <td width="248">clear screen</td>

  </tr>

  <tr>

   <td width="96">./prog</td>

   <td width="48"> </td>

   <td width="144">prog.exe</td>

   <td width="48"> </td>

   <td width="248">execute the program named prog.exe</td>

  </tr>

  <tr>

   <td width="96">rm</td>

   <td width="48"> </td>

   <td width="144">del</td>

   <td width="48"> </td>

   <td width="248">delete in the clean section of the makefile</td>

  </tr>

  <tr>

   <td width="96">cd</td>

   <td width="48"> </td>

   <td width="144">cd</td>

   <td width="48"> </td>

   <td width="248">change directory</td>

  </tr>

  <tr>

   <td width="96">ls</td>

   <td width="48"> </td>

   <td width="144">dir</td>

   <td width="48"> </td>

   <td width="248">view folder directory (files and folders)</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h1>CONCEPT: FORWARD DECLARATIONS</h1>

For this project <em>Forward Declarations</em> of classes are required since classes are co-dependent upon each other. A practical example of this co-dependency would be if a Doctor object contains a list of Patient objects, and each Patient object contains a list of Doctor objects. In this situation, do we declare the Doctor or the Patient first? The solution is to use <em>Forward Declarations</em> in each file as follows:




<em>// Doctor.h file</em>

#include “Patient.h”                                <em>// include Patient.h</em>

class Patient;                                           <em>// forward declaration of the Patient class</em> class Doctor {

<em>    </em>Patient *patient_list;                           <em>// array of Patient objects </em>

<em> </em>};

<em>// end of Doctor.h file</em>




<em>// Patient.h file</em>

#include “Doctor.h”                                <em>// include Doctor.h</em> class Doctor;                                                 <em>// forward declaration of Doctor class</em> class Patient {<em>  </em>

<em>    </em>Doctor *doctor_list;                             <em>// array of Doctor objects </em>

};

<em>// end of Patient.h file </em>

<strong> </strong>




<strong> </strong>

<strong>            </strong><em> </em>

<h1>CONCEPT: AGGREGATIONS AND INHERITANCE</h1>

This project will associate classes via Aggregations and Inheritance.




Within the scope of this project class aggregations will not require the big three since each object must have independent lifetimes and each object should not be cloned. This includes the majority of class types including <em>Airline</em>, <em>Airport</em>, <em>Flight</em>, <em>Person</em> and <em>Pilot</em>. Practically speaking <em>Flights</em> would be a logical candidate for cloning, but this is not a requirement for this project.




Furthermore, some use of inheritance/polymorphism will be required with the <em>Passenger</em> and <em>Pilot</em> classes since they are both of type <em>Person</em>.

<strong> </strong>

<h1>CLASS ASSOCIATIONS</h1>

<strong> </strong>

This project implements part of a simple flight reservation system using a variety of classes associated via aggregation and inheritance.

The is a simple list of classes and their data member associations (aggregation or inheritance) with other classes. Keep these associations in mind when considering dependencies and function requirements.   <strong>Airline  </strong>

<h1>Airport</h1>

<em>MyArray Flight* (arrivals) </em>

<em>MyArray Flight* (departures) </em>

<h1>Person</h1>

<em>MyArray Flight* (flights)</em>




<strong>Passenger</strong> <em>(inherits from Person)</em>




<strong>Pilot </strong><em>(inherits from Person)</em>




<h1>Flight</h1>

<em>Airline </em>

<em>Airport (source) </em>

<em>Airport (destination) </em>

<em>Pilot </em>

<em>MyArray Person* (passengers)</em>




<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1>PROJECT PHASES</h1>

This is the probably the most complex program you have attempted to develop thus far. For this reason, the project has been divided into five implementation <em>phases</em>. Five <em>Phase_#.cpp</em> files (1 to 5) have been provided to test your project at each <em>phase</em> of development.

Your project will run with only one <em>Phase_#.cpp</em> file at a time which is decided by editing your makefile.




<em>Phase_1.cpp</em> through <em>Phase_4.cpp</em> files <u>must not</u> be edited in your project submission to receive credit. <em>Phase_5.cpp</em> must be edited to match the client interface specifications of the <em>fifth phase</em>.




You should read this entire document (especially class specifications) before starting the project.




<strong>Watch the video to help you understand how to proceed and what is required.</strong>

<strong> </strong>

<h1>Phase 1: Implement the project skeleton</h1>

<strong> </strong>

<ol>

 <li>Make sure your Template Homework MyArray container compiles as is. If not fix it first.</li>

</ol>

Copy the template <em>MyArray</em> class code (nothing else) into a <em>MyArray.h</em> file.

<ol start="2">

 <li>Create empty .h and .cpp files for <u>all</u> of the files listed above.</li>

 <li><u>Only</u> add the following required code for each file (review the class descriptions): <em>include</em> statements

  <ol>

   <li><em>header guards</em> (#ifndef, def, #endif code)</li>

   <li><em>forward declarations</em> if required</li>

   <li>Basic class code including:

    <ol>

     <li>All data members except for <em>MyArray</em> objects</li>

     <li>Default constructor declarations in .h files, definitions in .cpp files (no other functions)</li>

    </ol></li>

   <li>Duplicate the downloaded <em>makefile</em> for easy copy/paste editing later on.</li>

   <li>It may help to remove any references to <em>Flight</em> in the <em>makefile</em> until you get all other files working.</li>

   <li>Repetitively compile and debug until the skeleton of the program is functioning.</li>

  </ol></li>

</ol>




<strong>Do not advance until Phase 1 compiles perfectly.</strong>

<em> </em>

<h1>Phase 2: Constructors and Output</h1>

<strong> </strong>

<ol>

 <li>Modify the <em>makefile</em> to run <em>cpp</em> instead of <em>Phase_1.cpp</em>.</li>

 <li>Comment out and uncomment parts of <em>cpp</em> as you work through this <em>phase</em>.</li>

 <li>Complete all constructor functions with exception to <em>MyArray</em> object content for these classes:</li>

</ol>

<em>Airline</em>, <em>Airport</em>, <em>Person</em>, <em>Pilot</em>, <em>Passenger</em>, <em>Flight</em>

<ol start="4">

 <li>Complete <em>getName</em> accessor function declarations and definitions for the following classes:</li>

</ol>

<em>Airline</em>, <em>Airport</em>, <em>Pilot</em>, <em>Passenger</em>

<ol start="5">

 <li>Complete the <em>overloaded &lt;&lt; operator</em> functions for the following classes: <em>Airport</em>, <em>Passenger</em>, <em>Pilot</em>, <em>Flight</em></li>

</ol>

<strong> </strong>

<strong>Do not advance until Phase 2 compiles perfectly.</strong>

<strong> </strong>

<h1>Phase 3: Accessors and Mutators</h1>

<strong> </strong>

<ol>

 <li>Modify the <em>makefile</em> to run <em>cpp</em> instead of <em>Phase_2.cpp</em>.</li>

 <li>Add the remaining specified <em>set</em> and <em>get</em> (not add/remove) functions for the following classes:</li>

</ol>

<em>Airline</em>, <em>Airport</em>, <em>Flight</em>, <em>Passenger</em>, <em>Person</em>, <em>Pilot</em>

<ol start="3">

 <li>For the moment avoid any code which requires add/remove functions for <em>MyArray</em> <em>objects</em>.</li>

</ol>




<strong>Do not advance until Phase 3 compiles perfectly. </strong>

<h1>Phase 4: MyArray Objects and Functions</h1>

<strong> </strong>

<ol>

 <li>Modify the <em>makefile</em> to run <em>cpp</em> instead of <em>Phase_3.cpp</em>.</li>

 <li>Add <em>MyArray</em> objects as specified to the following classes:</li>

</ol>

<em>Airport</em>, <em>Person</em>, <em>Flight</em>

<ol start="3">

 <li>Add <em>addArrival</em>, <em>removeArrival</em>, <em>addDeparture</em>, <em>removeDeparture</em> functions to class <em>Airport</em>.</li>

</ol>

Update the <em>Flight</em> multi-parameter constructor to work with these new functions.

<ol start="4">

 <li>Add Pilot <em>addFlight</em> and <em>removeFlight</em></li>

</ol>

Add Passenger <em>addFlight</em> and <em>removeFlight</em> functions.

Add Flight <em>addPassenger</em> and <em>removePassenger</em> functions

Add Flight <em>getPassenger</em>, <em>listPassengers</em> and <em>getNumPassengers</em> functions     Note that all of these functions and similar and are dependent upon each other.

You need to update all of these functions progressively and simultaneously while testing for      compiler errors.

<ol start="5">

 <li>Add any remaining class functions (check all files and class specifications).</li>

</ol>




<strong>Do not advance until Phase 4 compiles perfectly.</strong>




<h1>Phase 5: Client Interface</h1>

<strong> </strong>

The client interface is a program that uses all classes of your project to build a flight reservation system.

<strong> </strong>

<ol>

 <li>Modify the <em>makefile</em> to run <em>cpp</em> instead of <em>Phase_4.cpp</em>.</li>

 <li>Modify <em>cpp</em> to create a flight reservation client interface.</li>

</ol>

See the Client Interface description at the end of this document (last two pages).

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1>CLASS SPECIFICATIONS</h1>

<strong> </strong>

<strong><u>Class Airline</u> </strong>

<strong>Data member:</strong>

<em>name</em> (string): name of the airline




<strong>Functions:</strong>

<ol>

 <li><em>default constructor </em></li>

 <li><em>one parameter constructor</em></li>

 <li><em>name mutator</em></li>

 <li><em>name accessor</em></li>

</ol>




<strong><u>Class Airport</u> </strong>

<strong>Data member:</strong>

<em>name</em> (string): name of the airport

<em>symbol</em> (string): 3 letter symbol, for example John F Kennedy is JFK <em>arrivals</em> (MyArray): MyArray of arriving flight object pointers <em>departures</em> (MyArray): MyArray of departing flight object pointers




<strong>Functions:</strong>

<ol>

 <li><em>default constructor</em></li>

 <li><em>two parameter constructor</em></li>

 <li><em>name mutator and accessor</em></li>

 <li><em>symbol mutator and accessor</em></li>

 <li><em>addArrival</em></li>

 <li>Call whenever a flight <em>destination</em> is set to this airport</li>

 <li>Check if a flight is in <em>arrivals</em> If so, add flight to <em>arrivals</em></li>

 <li><em>addDeparture</em></li>

 <li>Call whenever a flight <em>source</em> is set to this airport</li>

 <li>Check if a flight is in <em>departures</em> If so, add flight to <em>departures</em></li>

 <li><em>removeArrival </em></li>

 <li>Call whenever a flight d<em>estination</em> is no longer this airport</li>

 <li>Check if a flight is in the <em>arrivals</em> If so, remove flight from <em>arrivals</em></li>

 <li><em>removeDeparture</em></li>

 <li>Call whenever a flight s<em>ource</em> is no longer this airport</li>

 <li>Check if a flight is in <em>departures</em> If so, remove flight from <em>departures </em></li>

 <li><em>closeAirport</em></li>

 <li>All <em>flights</em> in <em>arrivals</em> and <em>departures</em> should have <em>source</em>/<em>destination</em> set to nullptr (use flight functions) j. <em>overloaded &lt;&lt; operator</em></li>

 <li>Print <em>name</em>, <em>symbol</em> and list <em>arrivals</em> and <em>departures</em>, if no <em>arrivals</em> or <em>departures</em> print <em>none</em>.</li>

</ol>




<strong><u>Class Person</u> </strong>

This is an abstract class which does not require a .cpp file, only a .h file.

<strong>Data member:</strong>

<em>name</em> (string): name of the airline




<strong>Functions:</strong>

<ol>

 <li><em>default constructor – inline definition </em></li>

 <li><em>one parameter constructor – inline definition</em></li>

 <li><em>name mutator – pure virtual function (defined in derived classes)</em></li>

 <li><em>name accessor – pure virtual function </em></li>

 <li><em>addFlight – pure virtual function </em></li>

 <li><em>removeFlight – pure virtual function </em></li>

</ol>

<em> </em>

<strong><u>Class Pilot</u> </strong>

This class is derived from class Person.

<strong>Data member:</strong>

<em>flights</em> (MyArray): MyArray of flight object pointers




<strong>Functions:</strong>

<ol>

 <li><em>default constructor </em></li>

 <li><em>one parameter constructor </em></li>

 <li><em>addFlight </em></li>

 <li>Check if a flight is in <em>flights</em></li>

 <li>If not, add flight to <em>flights</em></li>

 <li>Set <em>flight</em> <em>pilot</em> to this pilot (use flight functions)</li>

 <li><em>removeFlight </em></li>

 <li>Check if a <em>flight</em> is in <em>flights</em></li>

 <li>If so, remove <em>flight</em> from <em>flights</em></li>

 <li>Set <em>flight</em> <em>pilot</em> to nullptr (use flight functions)</li>

 <li><em>overloaded &lt;&lt; operator</em></li>

 <li>Print <em>name</em> and list <em>flights</em></li>

</ol>




<strong><u>Class Passenger</u> </strong>

This class is derived from class Person.

<strong>Data member:</strong>

<em>flights</em> (MyArray): MyArray of flight object pointers




<strong>Functions:</strong>

<ol>

 <li><em>default constructor </em></li>

 <li><em>one parameter constructor </em></li>

 <li><em>addFlight </em></li>

 <li>Check if a <em>flight</em> is in <em>flights</em></li>

 <li>If not, add <em>flight</em> to <em>flights</em></li>

 <li>Add <em>passenger</em> to <em>flight</em> <em>passenger</em>s (use flight functions)</li>

 <li><em>removeFlight </em></li>

 <li>Check if a <em>flight</em> is in <em>flights</em></li>

 <li>If so, remove <em>flight</em> from <em>flights</em></li>

 <li>Remove <em>passenger</em> from <em>flight</em> (use flight functions)</li>

 <li><em>cancelFlights</em></li>

 <li>Remove <em>passenger</em> from every <em>flight</em> in <em>flights</em> (use flight functions)</li>

 <li><em>overloaded &lt;&lt; operator</em></li>

 <li>Print passenger <em>name</em> and list the <em>flights</em></li>

</ol>

<strong> </strong>

<strong><u>Class Flight</u> </strong>

<strong>Data member: </strong>

<em>number</em> (int): the number of the flight <em>airline </em>(Airline): the flight airline <em>source</em> (Airport): the airport the flight will depart from <em>destination</em> (Airport): the airport the flight will arrive at <em>pilot</em> (Pilot): the pilot of the flight

<em>passengers</em> (MyArray): MyArray of <u>Person</u> object pointers







<strong>Functions:</strong>

<ol>

 <li><em>default constructor </em></li>

 <li><em>multi parameter constructor </em></li>

 <li>Initialize <em>number</em>, <em>airline</em>, <em>source</em>, <em>destination</em> and <em>pilot</em></li>

 <li>Add this <em>flight</em> to the <em>source</em> airport <em>departures </em>(do this after <em>Airport</em> class is complete)</li>

 <li>Add this <em>flight</em> to the <em>destination</em> airport <em>arrivals </em>(do this after <em>Airport</em> class is complete) Add this <em>flight</em> to the <em>pilot</em> <em>flights</em> (do this after <em>Pilot</em> class is complete)</li>

 <li><em>getNumber – return flight number</em></li>

 <li><em>getAirline </em>– return <em>airline</em> pointer</li>

 <li><em>getSource </em>– return <em>source</em> pointer</li>

 <li><em>getDestination </em>– return <em>destination</em> pointer</li>

 <li><em>getPilot </em>

  <ol>

   <li>If <em>pilot</em> is nullptr return “No Pilot”</li>

   <li>otherwise, return <em>pilot</em> <em>name</em> as string (use pilot functions)</li>

  </ol></li>

 <li><em>getPassenger</em> –

  <ol>

   <li>given an <em>index</em>, return a <em>Person</em> object reference to a <em>passenger</em> in <em>passengers</em></li>

  </ol></li>

 <li><em>setAirline – Airline</em> object as parameter</li>

 <li><em>setSource – Airport</em> object as parameter</li>

 <li><em>setDestination – Airport</em> object as parameter</li>

 <li><em>setPilot </em></li>

 <li><em>Pilot</em> object as parameter</li>

 <li>If replacing a <em>pilot</em>, remove this <em>flight</em> from old <em>pilot</em> <em>flights</em> Set <em>pilot</em> to new <em>pilot</em> and add <em>flight</em> to new <em>pilot</em> <em>flights</em></li>

 <li><em>nullPilot –</em> set <em>pilot</em> to nullptr</li>

 <li><em>nullSource –</em> set <em>source</em> to nullptr</li>

 <li><em>nullDestination –</em> set <em>destination</em> to nullptr</li>

 <li><em>addPassenger </em></li>

 <li>Accept a <em><u>Person</u></em> object by parameter.</li>

 <li>Check if <em>passenger</em> is in <em>passengers</em>.</li>

 <li>If not, add <em>passenger</em> to <em>passengers</em> and add <em>flight</em> to <em>passenger</em> <em>flights</em></li>

 <li><em>removePassenger </em></li>

 <li>Accept a <em><u>Person</u></em> object by parameter.</li>

 <li>Check if <em>passenger</em> is in <em>passengers</em>.</li>

 <li>If so, remove <em>passenger</em> from <em>passengers</em> and remove <em>flight</em> from <em>passenger</em> <em>flights</em></li>

 <li><em>listPassengers </em>– print a list of the passengers</li>

 <li><em>getNumPassengers</em> – return the number of passengers</li>

 <li><em>cancel </em></li>

 <li>Remove <em>flight</em> from <em>source</em> airport <em>departures</em>, set <em>source</em> to nullptr</li>

 <li>Remove <em>flight</em> from <em>destination</em> airport <em>arrivals</em>, set <em>destination</em> to nullptr</li>

 <li>Remove <em>flight</em> from <em>pilot flights</em>, set <em>pilot</em> to nullptr</li>

 <li>Remove <em>flight</em> from each<em> passenger flights </em>in<em> passengers</em></li>

 <li><em>overloaded &lt;&lt; operator</em></li>

 <li>Print <em>number</em>, <em>airline</em>, <em>source</em>, <em>destination</em>, <em>pilot</em> and list <em>passengers</em>.</li>

</ol>


































<h1>CLIENT INTERFACE</h1>

Modify the <em>Phase_5.cpp</em> file to implement a flight reservation client interface as specified below. The provided file implements a few global containers and a <em>read</em> function with some data to get you started

<strong>Watch the end of project video for a walk through of the client interface. </strong>




<h1>EXPECTATIONS/ CONCERNS</h1>

The description for the client interface is somewhat vague to provide some flexibility in implementation.




When modifying objects it is extremely <u>important</u> to update all associated objects. For example if you delete a <em>Flight</em> you have to update associated <em>MyArray</em> objects such as source object <em>departures</em>, destination object <em>arrivals</em>, pilot object <em>flights</em> and passenger object <em>flights</em>. Always consider how all associations will be impacted when modifying data.




Above all, it is important that the interface you code is easy to read, easy to understand and bug free. It is significantly better to code less with no bugs then to code more with tons of bugs.  <strong>CONTAINERS </strong>(provided In original <em>Phase_5.cpp</em> file)

<table width="527">

 <tbody>

  <tr>

   <td width="192"> AirlinesAirportsPassengersPilotsFlights<strong> </strong><strong>MENUS </strong> MAIN MENU:</td>

   <td width="335"> </td>

  </tr>

  <tr>

   <td width="192">1 Airports</td>

   <td width="335">(opens Airports submenu)</td>

  </tr>

  <tr>

   <td width="192">2 Flights</td>

   <td width="335">(opens Flights submenu)</td>

  </tr>

  <tr>

   <td width="192">3 Passengers</td>

   <td width="335">(opens Passengers submenu)</td>

  </tr>

  <tr>

   <td width="192">4 End program AIRPORTS SUBMENU</td>

   <td width="335">(end the program)</td>

  </tr>

  <tr>

   <td width="192">1 List Airports</td>

   <td width="335">(list <em>Airports</em> by index)</td>

  </tr>

  <tr>

   <td width="192">2 Create Airport</td>

   <td width="335">(create a new <em>Airport</em> name and symbol)</td>

  </tr>

  <tr>

   <td width="192">3 Delete Airport</td>

   <td width="335">(list <em>Airports</em>, select by index to delete)</td>

  </tr>

  <tr>

   <td width="192">4 Main Menu FLIGHTS SUBMENU</td>

   <td width="335">(return to <em>Main</em> <em>Menu</em>)</td>

  </tr>

  <tr>

   <td width="192">1 List Flights</td>

   <td width="335">(list <em>Flights</em> by index)</td>

  </tr>

  <tr>

   <td width="192">2 Add Flight</td>

   <td width="335">(create a new <em>Flight</em>, select all data members by index)</td>

  </tr>

  <tr>

   <td width="192">3 Delete Flight</td>

   <td width="335">(list <em>Flights</em>, select by index to delete)</td>

  </tr>

  <tr>

   <td width="192">4 Select Flight</td>

   <td width="335">(list <em>Flights</em> and select by index to open <em>Flight</em> <em>Submenu</em>)</td>

  </tr>

  <tr>

   <td width="192">5 Main Menu</td>

   <td width="335">(return to <em>Main</em> <em>Menu</em>)</td>

  </tr>

 </tbody>

</table>










<table width="580">

 <tbody>

  <tr>

   <td width="192">FLIGHT SUBMENU</td>

   <td width="388"> </td>

  </tr>

  <tr>

   <td width="192">1 Change Pilot</td>

   <td width="388">(list pilots, select by index to modify pilot)</td>

  </tr>

  <tr>

   <td width="192">2 Change Departure Airport</td>

   <td width="388">(list <em>Airports</em>, select by index to modify <em>source</em> <em>airport</em>)</td>

  </tr>

  <tr>

   <td width="192">3 Change Arrival Airport</td>

   <td width="388">(list <em>Airports</em>, select by index to modify <em>destination</em> <em>airport</em>)</td>

  </tr>

  <tr>

   <td width="192">4 Add Passenger</td>

   <td width="388">(list <em>Passengers</em>, select by index to add <em>Passenger</em>)</td>

  </tr>

  <tr>

   <td width="192">5 Remove Passenger</td>

   <td width="388">(list <em>Passengers</em>, remove by index to remove <em>Passenger</em>)</td>

  </tr>

  <tr>

   <td width="192">6 Flights Menu PASSENGER SUBMENU</td>

   <td width="388">(return to <em>Flights</em> <em>Submenu</em>)</td>

  </tr>

  <tr>

   <td width="192">1 List Passengers</td>

   <td width="388">(lists all <em>Passengers</em> in database)</td>

  </tr>

  <tr>

   <td width="192">2 Create Passenger</td>

   <td width="388">(create a new <em>Passenger</em> and add it to the <em>Passengers</em> container)</td>

  </tr>

  <tr>

   <td width="192">3 Delete Passenger</td>

   <td width="388">(lists <em>Passengers</em>, select by index to delete)</td>

  </tr>

  <tr>

   <td width="192">4 Main Menu</td>

   <td width="388">(return to <em>Main</em> <em>Menu</em>)</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h1>FUNCTIONS</h1>




These are a number of recommended functions you should implement to support menu actions in the <em>Phase_5.cpp</em> file. The purpose of these functions should be relatively obvious if you examine the menus. Many of these functions access the global containers to provide a list of options for the user to select from.




<em>listAirlines listAirports listFlights selectPilot selectSourceAirport </em>

<em>selectDestinationAirport addPassenger removePassenger </em>

<em>changeFlight (can use this to run the Flight Submenu or code it in Main) createAirport deleteAirport createPassenger </em>

<em>deletePassenger </em>

<em> </em>