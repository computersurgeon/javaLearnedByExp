# javaLearnedByExp

Core java {Abstraction/Encapsulation/Inheritance/Ploymorphism}
Advanced java {Collections/Generics/Threads/Lambda/Serialization}
Spring
Spring Boot
Hibernate
Servlet
Design Pattern
Maven



(I)BASICS
(1) Introduction/Basics on java
(2) JVM
(3) JAXB
(4) IDE
(5) Learned by experience in eclipse
(6) Java/Javac/Javaw/Javaws
(7) DataTypes
(8) Operators
(9) Java library
(10) SWT, GWT, SWING, XWT, JavaFX - WebTool kit
(11) Short cut key in eclipse
(12) Generics in java
(13) Swing main method() & Swing related
(14) DataBase Helper (Connection, Properties, Statement, CallableStatement, PreparedStatement,ResultSet )
(15) String Handling
(16) Spring Framework , DispatcherServlet, WebApplicationInitializer (web.xml ! mandate)
(17) Learn Maven By Experience
(18) Tools
(19) About EJB, SPRING, Applet, Servlet, Struts, JavaEE, J2EE
(20) EXTJS
(20.a) JavaScript
(21) Learn Hibernate
(21.a) DTO Vs DAO
(22) SVN
(23) Java webservice JAX-WS/JAX-RS
(24) EJB
(25) Drools
(26) nodejs
(27) API vs SPI
(28) collection Set/List/Queue/Map
(Appendix 1) Achievement
(Appendix 2) ERROR
---------------------------------------------------------------------------------------------------------------------------------------------
(I)BASICS
---------------------------------------------------------------------------------------------------------------------------------------------
Difference between import/extends/implemets
1.) import is used to get ride of full name spacequialifer and we ca use the features of the importing class without modify
2.) extends is used to override/inherit feature of a class
3.) implements is used to implement all the methods used in interface. one interface can extends another interface
4.) const is a reserved keyword but unused in java
5.) final modifier means that you cannot change variable, i.e. reference to your object, i.e. assign other value to the same variable. You can however change the state of object itself. 
6.) Java and Javax it's a extension of java

When to use new classObject and when to use ClassObject without new
------------------------------------------------------------------
Class Variable Vs Instance variable
class Animal()
{
    private int _numberOfLegs = 4; //This is an instance variable
    private static int numberOfAnimals = 0; //This is a class variable
 
    public Animal() {
        //code goes here
 
        //this increases the numberOfAnimals on creation of new one
        ++numberOfAnimals;
    }
 
    public int numberOfLegs() {
        return _numberOfLegs;
    }
}
Difference between class and instance variables
Now, it should be clear what the difference between instance and class variables is. Class variables only have one copy that is shared by all the different objects of a class, whereas every object has it’s own personal copy of an instance variable. So, instance variables across different objects can have different values whereas class variables across different objects can have only one value.

---------------------------------------------------------------------------------------------------------------------------------------------
(1) JAVA
---------------------------------------------------------------------------------------------------------------------------------------------
In the Java programming language, all source code is first written in plain text files ending with the .java extension. Those source files are then compiled into .class files by the javac compiler. A .class file does not contain code that is native to your processor; it instead contains bytecodes — the machine language of the Java Virtual Machine1 (Java VM). The java launcher tool then runs your application with an instance of the Java Virtual Machine.
----------------------------------------------------------------------------------------------------------------------------------------------
(2) JVM
---------------------------------------------------------------------------------------------------------------------------------------------
A Java virtual machine (JVM) is a virtual machine that can execute Java bytecode. It is the code execution component of the Java platform.

Programs intended to run on a JVM must be compiled into Java bytecode, a standardized portable binary format which typically comes in the form of .class files (Java class files). A program may consist of many classes in different files. For easier distribution of large programs, multiple class files may be packaged together in a .jar file (short for Java archive).

The Lifetime of a Java Virtual Machine

A runtime instance of the Java virtual machine has a clear mission in life: to run one Java application. When a Java application starts, a runtime instance is born. When the application completes, the instance dies. If you start three Java applications at the same time, on the same computer, using the same concrete implementation, you'll get three Java virtual machine instances. Each Java application runs inside its own Java virtual machine. 

Java's default heap size limit is 128MB.
This can be increased by supply the following as arguments.

-Xms<size> -Xms<n>K/-Xmx<n>M
specifies the initial Java heap size and

-Xmx<size>
the maximum Java heap size. 
----------------------------------------------------------------------------------------------------------------------------------------------
(3) JAXB - (JAVA Architecture for XML Binding)
---------------------------------------------------------------------------------------------------------------------------------------------
The act of converting an XML document to and from an java object/ java class. This conversion process is also known as XML Marshalling, or XML Serialization.

Java Architecture for XML Binding (JAXB) allows Java developers to map Java classes to XML representations. JAXB provides two main features: the ability to marshal Java objects into XML and the inverse, i.e. to unmarshal XML back into Java objects. In other words, JAXB allows storing and retrieving data in memory in any XML format, without the need to implement a specific set of XML loading and saving routines for the program's class structure. It is similar to xsd.exe and XmlSerializer in the .NET Framework.
----------------------------------------------------------------------------------------------------------------------------------------------
(4) IDE - NetBeans Vs Eclipse
---------------------------------------------------------------------------------------------------------------------------------------------
NetBeans
Eclipse
IntilliJ IDEA


NeatBeans developed by SUN - well known for its built in packages instead of plugins, have ver nice GUI builder.
Eclipse developed by IBM - Well known for its available plugin, Release early and mostly used by developers. 
IntelliJ IDEA module file (*.iml)
---------------------------------------------------------------------------------------------------------------------------------------------
(5) learned by experience in eclipse:
---------------------------------------------------------------------------------------------------------------------------------------------
to install new plugin / software within eclipse 
Go to -> HELP -> Install new software
Mention the URL and its name then eclipse will take care of installing it.

ctrl + mouse left click / F3 key to GO_TO_DEFINITION.
ctrl+E/ctrl+f6 -> to switch between tabs/editors
ctrl + shift + / -> to comment a block
ctrl+B -> build all	
ctrl+f11 -> Run selected project
ctrl+shift+num_divide -> collapse definition
ctrl+shift+num_multiply -> expand definition
ctrl+shift+F -> format code
ctrl+shift+L -> shortcut keys Preference
ctrl+w -> close edit window / current tab
ctrl+shift+p -> goes to matching bracket
Alt+f5 -> Maven project force update



Eclipse project files (.project and .classpath)

switch("String") is not supported untill 1.6 compiler.

NetBeans is bulky than the Eclipse. Usually consume lots of system resources (memory)

How to install missing plugins in eclipse
-----------------------------------------
1.) Maven
2.) Spring

two different ways to do that
1.) use Help-> Install new software . here mention the update site URL. All related plugin exposed can be consumed and automatically gets installed. Once done restart eclipse.

2.) Help-> market place search for the required plugin and cli

----------------------------------------------------------------------------------------------------------------------------------------------
(6) Java/Javac/Javaw/Javaws
---------------------------------------------------------------------------------------------------------------------------------------------
C:\>javac HelloWorld.java
will create a HelloWorld.class
C:\>java HelloWorld.class
will print "HelloWorld"

    1.) The java tool launches a Java application. It does this by starting a Java runtime environment, loading a specified class, and invoking that class's main method.
    2.) The javaw command is identical to java, except that with javaw there is no associated console window. Use javaw when you don't want a command prompt window to appear.
	3.) javaws is for java web start applications, applets
	
----------------------------------------------------------------------------------------------------------------------------------------------(7) DataTypes
---------------------------------------------------------------------------------------------------------------------------------------------
Data Type 	Default Value (for fields)
byte 		0
short 		0
int 		0
long 		0L
float 		0.0f
double 		0.0d
char 		'\u0000'
String (or 
any object)   	null
boolean 	false	
final 
Static
Super 
Super Vs this

Array with eg:-
int[] anArray = { 
    100, 200, 300,
    400, 500, 600, 
    700, 800, 900, 1000
};
String[][] names = {
            {"Mr. ", "Mrs. ", "Ms. "},
            {"Smith", "Jones"}
        };

---------------------------------------------------------------------------------------------------------------------------------------------
(8) Operators
---------------------------------------------------------------------------------------------------------------------------------------------
==      equal to
!=      not equal to
>       greater than
>=      greater than or equal to
<       less than
<=      less than or equal to

Conditional Operators
---------------------
&& Conditional-AND
|| Conditional-OR		

forloop
-------
class EnhancedForDemo {
    public static void main(String[] args){
         int[] numbers = 
             {1,2,3,4,5,6,7,8,9,10};
         for (int item : numbers) {
             System.out.println("Count is: " + item);
         }
    }
}

final
-----
The final keyword has more than one meaning :

    a final class cannot be extended
    a final method cannot be overridden
    final fields, parameters, and local variables cannot change their value once set
	
Static
------
Static means it belongs to the class not an instance, this means that there is only one copy of that variable/method shared between all instances of a particular Class.

public class MyClass {
    public static int myVariable = 0; 
	private void method1() throws Exception
	{	}
	private void method2() throws Exception
	{	}
}

//Now in some other code creating two instances of MyClass
//and altyering the variable will affect all instances

MyClass instance1 = new MyClass();
MyClass instance2 = new MyClass();

MyClass.myVariable = 5;  //This change is reflected in both instances	

Super
-----
it refers the immediate paren't property.
super()//refers parent's constructor
super.getMusic();//refers to the parent's method

Super Vs this
-------------
super is used to access methods of the base class while this is used to access methods of the current class.

----------------------------------------------------------------------------------------------------------------------------------------------
(9) Java library (Java Foundation Classes (JFC))
---------------------------------------------------------------------------------------------------------------------------------------------
java.sql.*; - all dbhelper class like Connection, statement, CallableStatement, Properties, ResultSet are available
java.awt.*; - Abstract Window ToolKit (Java Graphical User Interface (GUI) components)
javax.swing.*; - Java Graphical User Interface (GUI) components & "lightweight" components. Swing supports a wider range of features.

GridLayout(int rows, int cols, int hgap, int vgap)
    rows - the rows, with the value zero meaning any number of rows.
    cols - the columns, with the value zero meaning any number of columns.
	
    a final class cannot be extended
    a final method cannot be overridden
    final fields, parameters, and local variables cannot change their value once set
	
	frmFileLayoutParser.getContentPane().setCursor(Cursor.getPredefinedCursor(Cursor.WAIT_CURSOR));
	frmFileLayoutParser.getContentPane().setCursor(Cursor.getPredefinedCursor(Cursor.DEFAULT_CURSOR));
----------------------------------------------------------------------------------------------------------------------------------------------
(10) SWT, GWT, SWING, XWT, JavaFX
---------------------------------------------------------------------------------------------------------------------------------------------
GWT is strictly for developing web apps

If you want to write a regular Java GUI, your choices are

    SWT
    Swing
    JavaFX
GWT
It is a product of Google and has the tools which are used to not only to make but also maintain the web written in java script it supports everything that is written in java language.

SWT
It is a graphical tool kit which is used to maintain the websites and is a product of IBM but now it is maintained and looked after by the Eclipse foundation.

Swing
It is also a graphical tool kit which is used by the users and is known primary for the java language. It is more compact and more reliable than the AWT as they do not need any code.

AWT
It is the original java based tool kit which is used for the graphical as well as the user interface. This tool kit is also used for many java profiles and is a part of Java Foundation Class.

----------------------------------------------------------------------------------------------------------------------------------------------
(11)  Short cut key in eclipse
---------------------------------------------------------------------------------------------------------------------------------------------
CTRL+E (for a list of editor)
CTRL+F6 (for switching to the next editor through a list)
F3 (go to definition)
F4 (opens Type Hierarchy), click F4 on interface to look the implementation
F11 (RUN)
Ctrl+F2 (TERMINATE)
F5 - step into
F6 - step over
F7 - step to next break point
----------------------------------------------------------------------------------------------------------------------------------------------
package 

public class Contact implements Serializable  {

 private String name;
 private String email;


 public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getEmail() {
     return email;
    }

    public void setEmail(String email){
     this.email = email;
    }
}

    When should i implment Serializble interface?
    Why do we do that?
    Does it give any advantages or security?

implement the Serializable interface when you need to store a copy of the object, send them it to another process on the same system or over the network.
Because you want to store or send an object.Serializable classes are useful when you want to persist instances of them or send them over a wire.
It makes storing and sending objects easy. It has nothing to do with security.
----------------------------------------------------------------------------------------------------------------------------------------------
(12) Generics in java (TypeSafe)
---------------------------------------------------------------------------------------------------------------------------------------------
<T> : Generics avoids explicit conversion of an object's type, instead we pass the object as param.

Object obj = 13;
int i = 13; // cannot conervt objtect to int so
int i = (int)13; to avoid explicit conversion
Object<int> obj = 13;
int i = obj;

ArrayLilst<Integer> obj = new ArrayList<Interger>();

public class Animal{}
Public class Dog extends Animal{}

Animal[] animalsArray = { new Animal(), new Dog()};
Dog[] dogsArray = {new Dog(), new Dog()};

List<Object> objectsList = new ArrayList<Object>();
List<Animal> animalsList = new Arrays.asList(animalsArray);
List<Dog> dogsList = new Array.asList(dogsArray);

List<? extends Animal> extendedList = animalsList; // dogsList;
List<? super Animal> superList = objectList; // animalList;


Collection Interface:
---------------------
The Collection interface is the root interface for the Java collections hierarchy. It is extended by the List, Set, and the SortedSet interfaces. The Collection interface is used to represent a group of objects, or elements. Typically, it represents data items that form a natural group. Some collection allows duplicate elements while others do not. It consists of both ordered and unordered elements.
The declaration of the Collection interface is shown as:
public interface Collection<E>.. 

Table of the ordered and unordered Collection interfaces shown as:
 Interface name 	 Ordered 	 Allows duplicates 	 Maps key to object
 Collection 	 	 No 	 	Yes 	 			No
 List 	 			Yes 	 	Yes 	 			No
 Set 	 			 No 	 	No 	 				No
 Map 	 			No 	 	 	No 	 				Yes
 SortedSet 	 		Yes 	 	No 	 				No
 SortedMap 	 		Yes 	 	No 	 				Yes
 
What is difference between Enumeration and Iterator interface?
Enumeration is twice as fast as Iterator and uses very less memory. Enumeration is very basic and fits to basic needs. But Iterator is much safer as compared to Enumeration because it always denies other threads to modify the collection object which is being iterated by it.
Iterator takes the place of Enumeration in the Java Collections Framework. Iterators allow the caller to remove elements from the underlying collection that is not possible with Enumeration. Iterator method names have been improved to make it’s functionality clear.


List is an ordered collection and can contain duplicate elements. You can access any element from it’s index. List is more like array with dynamic length.
A Map is an object that maps keys to values. A map cannot contain duplicate keys: Each key can map to at most one value.

List<Object>
List<? extends Object> lst = new ArrayList<Object>();
ArrayList<Object>
Hash<Object,Object>
HashMap<String, List<String>>
HashMap<String, ArrayList<ArrayList<Object>>>
HashSet Vs TreeSet
Vector implements a dynamic array. It is similar to ArrayList, but with two differences:
Vector is synchronized.
Vector contains many legacy methods that are not part of the collections framework.
Vector proves to be very useful if you don't know the size of the array in advance, or you just need one that can change sizes over the lifetime of a program.
Class java.util.Vector
Vector( )
Vector(int size)
Vector(int size, int incr)
Vector(Collection c)

java.util.concurrent.BlockingQueue;
BlockingQueue<T> queue = ArrayBlockingQueue(n) //n being bonded capacity of queue
BlockingQueue<T> queue = LinkedBlockingQueue() //This queue's capacity grows as it get populated and drained
Use producer & consumer that implements Runnable Interface

put() : Inserts the specified element into this queue, waiting if necessary for space to become available.
offer(): Inserts the specified element into this queue, waiting up to the specified wait time if necessary for space to become available.
take() : Retrieves and removes the head of this queue, waiting if necessary until an element becomes available.
poll() : Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available
peek() : Retrieves, but does not remove, the head of this queue, or returns null if this queue is empty.
contains() : Returns true if this queue contains the specified element. More formally, returns true if and only if this queue contains at least one element e such that o.equals(e).

HashSet is much faster than TreeSet (constant-time versus log-time for most operations like add, remove and contains) but offers no ordering guarantees like TreeSet.
HashSet:

    class offers constant time performance for the basic operations (add, remove, contains and size).
    it does not guarantee that the order of elements will remain constant over time
    iteration performance depends on the initial capacity and the load factor of the HashSet.
        It's quite safe to accept default load factor but you may want to specify an initial capacity that's about twice the size to which you expect the set to grow.

TreeSet:

    guarantees log(n) time cost for the basic operations (add, remove and contains)
    guarantees that elements of set will be sorted (ascending, natural, or the one specified by you via it's constructor)
    doesn't offer any tuning parameters for iteration performance
    offers a few handy methods to deal with the ordered set like first(), last(), headSet(), and tailSet() etc
	Map<String,String> obj = new TreeMap<String,String>();
	 Map<String, Set<String>> dictionary = new TreeMap<>();
    Set<String> a = new TreeSet<>(Arrays.asList("Actual", "Arrival", "Actuary"));
    Set<String> b = new TreeSet<>(Arrays.asList("Bump", "Bravo", "Basic"));
    dictionary.put("B", b);
    dictionary.put("A", a);
    System.out.println(dictionary);
	output:
	{A=[Actual, Actuary, Arrival], B=[Basic, Bravo, Bump]} 

Important points:

    Both guarantee duplicate-free collection of elements
    It is generally faster to add elements to the HashSet and then convert the collection to a TreeSet for a duplicate-free sorted traversal.
    None of these implementation are synchronized. That is if multiple threads access a set concurrently, and at least one of the threads modifies the set, it must be synchronized externally.
    LinkedHashSet is in some sense intermediate between HashSet and TreeSet. Implemented as a hash table with a linked list running through it, however it provides insertion-ordered iteration which is not same as sorted traversal guaranteed by TreeSet.

So choice of usage depends entirely on your needs but I feel that even if you need an ordered collection then you should still prefer HashSet to create the Set and then convert it into TreeSet.

    e.g. Set<String> s = new TreeSet<String>(hashSet);

1.Hash set allow null object

2.Tress set will not allow null object .if you try to add null value i will be throw null pointer exception

3.Hash set much faster than tree set.
	
----------------------------------------------------------------------------------------------------------------------------------------------
(13) Swing main method()
---------------------------------------------------------------------------------------------------------------------------------------------

public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					FileLayoutParserUI window = new FileLayoutParserUI();
					window.frmFileLayoutParser.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

public FileLayoutParserUI() {
initialize();
}

private void initialize(){
JFrame(); // screen/window
 JPanel();// add this to JFrame
 JTabbedPane(); // add this to JPanel
}

JButton
-------
JButton btn = new JButton();
btn.addActionListener(new ActionListener(){
public void actionPerformed(ActionEvent e){}
});
	
DataTable/Grid population in java
---------------------------------
// using Table Model in java 
// addColumn
// addRow
// setModel

List<ArrayList<Object>> data;
List<String> columns;
DefaultTableModel dataModel = (DefaultTableModel)table.getModel();
for (String columnName : columns) {dataModel.addColumn(columnName);}
for (ArrayList<Object> rowData : data) {dataModel.addRow(rowData.toArray());}
table.setModel(dataModel);

import javax.swing.table.DefaultTableModel;
private JTable tableFilenameMap;
	public void setFileMapTableData(HashMap<String, String> fileMap) {
		DefaultTableModel dmodel = new DefaultTableModel();
		dmodel.addColumn("File Name");
		dmodel.addColumn("Table Name");
		for (Map.Entry<String, String> kv : fileMap.entrySet()) {
			Object[] data = new Object[] { kv.getKey(), kv.getValue() };
			dmodel.addRow(data);
		}
		this.tableFilenameMap.setModel(dmodel);
	}
---------------------------------------------------------------------------------------------------------------------------------------------
(14) DataBase Helper (Connection, Properties, Statement, CallableStatement, PreparedStatement,ResultSet )
---------------------------------------------------------------------------------------------------------------------------------------------
import java.sql.*;

statement.executeQuery()
statement.executeUpdate()
statement.execute();

Resultset is the only way to get scalar value too.
	
	Connection conn = null;
	Statement stmt = null;
	CallableStatement callableStatement = null;
	
	try{
	Class.forName("oracle.jdbc.driver.OracleDriver");
	Properties connectionProps = new Properties();
	connectionProps.put("user", "bketl");
			connectionProps.put("password", "bketldev");
			conn = DriverManager.getConnection("jdbc:oracle:thin:@//erid-scan:1521/OEERID", "bketl","bketldev");
			String query ="";
			stmt = conn.createStatement();
			ResultSet rs = stmt.executeQuery(query); this is used for select alone
			//stmt.executeUpdate(); this is used for DML
			
			callableStatement = conn.prepareCall("{call insertDBUSER(?,?,?,?)}"); //"{call procedure_name(param1,param2,param3,param4)}"
			callableStatement.setInt(1, 1000);
			callableStatement.setString(2, "mkyong");
			callableStatement.setString(3, "system");
			callableStatement.setDate(4, new java.sql.Date(today.getTime()));
			callableStatement.executeUpdate();
			
			while (rs.next()) {}
	
	}
	catch(Exception e){
	}
	finally{
	}
	
	
	Getting more than one resultset or output param from statement execution
	-------------------------------------------------------------------------
	boolean hadResultSet = statement.execute();
	while(hadResultSet){
	ResultSet rs = statement.getResultSet();
	hadResultSet = statement.getMoreResults();
	}
	
	Setting & Getting input/ouput param index based & name based
	--------------------------------------------
	
	cStmt.setString(1, "abcdefg");
	cStmt.setString("inputParameter", "abcdefg");
	cStmt.setInt(2, 1);
	cStmt.setInt("inOutParam", 1);
	
	
	statement.registerOutParameter(2, Types.INTEGER);
	statement.getInt(1);
	statement.registerOutParameter("inOutParam", Types.INTEGER);
	statement.getInt("inputparam");
	
----------------------------------------------------------------------------------------------------------------------------------------------
JAVA Terminology
----------------
POI stands in this case for "Poor Obfuscation Implementation"
Obfuscated code is source or machine code that has been made difficult to understand for humans.
deliberately - with intention.
---------------------------------------------------------------------------------------------------------------------------------------------
(15) String Handling
---------------------------------------------------------------------------------------------------------------------------------------------
Replacing non-printable characters
Range.stripFields(tablePar.text()).replaceAll("\\P{Print}", "");


${ERIDB_PASS_CONN}

---------------------------------------------------------------------------------------------------------------------------------------------
(16) Spring Framework
---------------------

Explaing the "flow" of a request in a Spring Web MVC application.

When sending a request to your application the following happens:

The request arrives at your server (e.g. Tomcat). Depending on the context path in the url the server decides to which application the request belongs.
Depending on the url and the servlet mapping in the web.xml file of your application the server knows which servlet should handle the request.
The request is passed to the servlet filter chain which can modify or reject requests
The servlet takes control over the request. In case of your Spring application the spring Dispatcherservlet receives the request. Now Spring kicks in
The request is processed by mvc intercepters preHandle methods
The request is mapped to a controller based on the url. The corresponding controller method will be called.
Your controller is processing the request. Many different responses can be returned in controllers (jsp, pdf, json, redirects, etc.). For now i assume you want to render a simple jsp view. Result of the controller are two things: a model and a view. The model is a map that contains the data you want to access later in your view. The view at this stage is most of the time a simple string containing a view name.
Registered springs mvc interceptors can kick in again using the postHandle method (e.g. for modifying the model)
The 'view' result of your controller is resolved to a real View using a ViewResolver. Depending on the ViewResolver the result can be jsp page, a tiles view, a thymeleaf template or many other 'Views'. In your case the ViewResolver resolves a view name (e.g. 'myPage') to a jsp file (e.g. /WEB-INF/jsp/myPage.jsp)
The view is rendered using the model data returned by your controller
The response with the rendered view will be passed to mvc interceptors again (afterCompletion method)
The response leaves the dispatcher servlet. Here ends spring land.
The response passes servlet filters again
The response is send back to client


web.xml
-------
If you do not want to go with default filename as [servlet-name]-servlet.xml and default location as WebContent/WEB-INF, you can customize this file name and location by adding the servlet listener ContextLoaderListener in your web.xml file as follows:
<web-app...>

<!-------- DispatcherServlet definition goes here----->
....
<context-param>
   <param-name>contextConfigLocation</param-name>
   <param-value>/WEB-INF/HelloWeb-servlet.xml</param-value>
</context-param>

<listener>
   <listener-class>
      org.springframework.web.context.ContextLoaderListener
   </listener-class>
</listener>
</web-app>


The technology that Spring is most identified with is Inversion of Control (or IoC), and specifically the Dependency Injection flavor of IoC. Spring is often thought of as an Inversion of Control container, although in reality it is much more.

Inversion of Control is best understood through the term the "Hollywood Principle," which basically means "Don't call me, I'll call you."

it has become popular in the Java community as an alternative to, replacement for, or even addition to the Enterprise JavaBean (EJB) model

IOC
---
In software engineering, inversion of control (IoC) is a programming technique, expressed here in terms of object-oriented programming, in which object coupling is bound at run time by an assembler object and is typically not known at compile time using static analysis.

DI
---
What is dependency injection exactly? Let's look at these two words separately. Here the dependency part translates into an association between two classes. For example, class A is dependent on class B. Now, let's look at the second part, injection. All this means is that class B will get injected into class A by the IoC.

Aspect Oriented Programming (AOP):
----------------------------------
One of the key components of Spring is the Aspect oriented programming (AOP) framework. The functions that span multiple points of an application are called cross-cutting concerns and these cross-cutting concerns are conceptually separate from the application's business logic. There are various common good examples of aspects including logging, declarative transactions, security, and caching etc.

The key unit of modularity in OOP is the class, whereas in AOP the unit of modularity is the aspect. Whereas DI helps you decouple your application objects from each other, AOP helps you decouple cross-cutting concerns from the objects that they affect.

DispatcherServlet 
-----------------
The job of the DispatcherServlet is to take an incoming URI and find the right combination of handlers (generally methods on Controller classes) and views (generally JSPs) that combine to form the page or resource that's supposed to be found at that location.

I might have

a file /WEB-INF/jsp/pages/Home.jsp
and a method on a class
@RequestMapping(value="/pages/Home.html")
private ModelMap buildHome() {
    return somestuff;
}
The Dispatcher servlet is the bit that "knows" to call that method when a browser requests the page, and to combine its results with the matching JSP file to make an html document.

How it accomplishes this varies widely with configuration and Spring version.

There's also no reason the end result has to be web pages. It can do the same thing to locate RMI end points, handle SOAP requests, anything that can come into a servlet.

WebApplicationInitializer
-------------------------
public class WebMVCApplicationInitializer implements WebApplicationInitializer {

    public void onStartup(ServletContext servletContext) {
      ServletRegistration.Dynamic servletReg = 
        servletContext.addServlet("dispatcher", new DispatcherServlet());
      servletReg.setLoadOnStartup(1);
      servletReg.addMapping("*.REQUEST");
    }
}
---------------------------------------------------------------------------------------------------------------------------------------------
(17) Learn Maven By Experience
-------------------------------
How to push Maven to Nexus
1.) SnapShot version - this version is for test environment
2.) Release version - this version is for production

Project Object Model(POM.xml)
-----------------------------
The fields groupId, artifactId, version are all required fields. These fields act much like an address and timestamp and marks a specific place in a repository.
The name of the project is given by artifactId generally. There may live many projects under the same group. The artifactID along with the groupId, create a key that separates this project from every other project in the world. In the discussed example, my-project lives in $M2_REPO/org/codehaus/mojo/my-project .

The groupId:artifactId combination denotes a single project but they cannot define which particular version of that project we are talking about. In software world, we have version numbers to differentiate the versions. Version no is used within an artifact's repository to separate versions from each other. my-project version 1.0 files will reside at: $M2_REPO/org/codehaus/mojo/my-project/1.0 . 

Examples
--------
<dependency>
		<groupId>org.apache.pig</groupId>
		<artifactId>pig</artifactId>
		<version>0.11.1</version>
	</dependency>
    <dependency>
		<groupId>org.apache.pdfbox</groupId>
		<artifactId>pdfbox</artifactId>
		<version>1.8.2</version>
	</dependency>
    <dependency>
		<groupId>rhino</groupId>
		<artifactId>js</artifactId>
		<version>1.7R2</version>
	</dependency>
	
	
ERROR : 
-------
Multiple annotations found at this line:
	- Plugin execution not covered by lifecycle configuration: org.apache.maven.plugins:maven-compiler-plugin:3.1:testCompile (execution: default-testCompile, phase: test-	 compile)
	- Plugin execution not covered by lifecycle configuration: org.apache.maven.plugins:maven-compiler-plugin:3.1:compile (execution: default-compile, phase: compile)
	- CoreException: Could not calculate build plan: Plugin org.apache.maven.plugins:maven-compiler-plugin:3.1 or one of its dependencies could not be resolved: Failed to read 
	
Solution :
----------
1.) Clean repository i.e., delete all folders 
2.) update settings.xml with the following information
<proxy>
      <id>optional</id>
      <active>true</active>
      <protocol>http</protocol>
      <host>proxy.pershing.com</host>
      <port>8080</port>
      <nonProxyHosts>localhost</nonProxyHosts>
    </proxy>	
3.) Alt+F5 force the project to download dependencies.
4.) Make sure you have <?xml version="1.0"?>
5.) Right click on error and use QUICK FIX

// The following code enables the capability of removing web.xml from web application
PUBLIC CLASS WEBMVCAPPLICATIONINITIALIZER IMPLEMENTS 
  WEBAPPLICATIONINITIALIZER {

    PUBLIC VOID ONSTARTUP(SERVLETCONTEXT CONTAINER) {
      SERVLETREGISTRATION.DYNAMIC REGISTRATION = 
        CONTAINER.ADDSERVLET("DISPATCHER", NEW DISPATCHERSERVLET());
      REGISTRATION.SETLOADONSTARTUP(1);
      REGISTRATION.ADDMAPPING("*.REQUEST");
    }
}

---------------------------------------------------------------------------------------------------------------------------------------------
(18) Tools
----------
Jetty - Web server and java servlet containser
Groovy - Groovy is an object-oriented programming language for the Java platform. It is a dynamic language with features similar to those of Python, Ruby, Perl, and Smalltalk. It can be used as a scripting language for the Java Platform, is dynamically compiled to Java Virtual Machine (JVM) bytecode, and interoperates with other Java code and libraries. Groovy uses a Java-like curly-bracket syntax. Most Java code is also syntactically valid Groovy.
Grails - a Groovy web framework
---------------------------------------------------------------------------------------------------------------------------------------------
(19) About EJB, SPRING, Applet, Servlet, Struts, JavaEE, J2EE

Servlet life cycle (init, perform, destroy)
-------
While tomcat starts (init gets triggred)
Perform serves the request in between init and destroy
While tomact shuts down (destroy gets triggred)

An applet that runs on a server, typically within Java.

A servlet is simply a class which responds to a particular type of network request - most commonly an HTTP request. Basically servlets are usually used to implement web applications - but there are also various frameworks which operate on top of servlets (e.g. Struts) to give a higher-level abstraction than the "here's an HTTP request, write to this HTTP response" level which servlets provide.

Servlets run in a servlet container which handles the networking side (e.g. parsing an HTTP request, connection handling etc). One of the best-known open source servlet containers is Tomcat.

TOMCAT STARTUP ISSUE
--------------------
SEVERE: A child container failed during start

History: J2EE was horrible, so Spring helped!
---------------------------------------------
J2EE was horrible. So much XML configuration, so many interfaces, and so lame application servers. This is why the Spring framework was created. It solved many problems of J2EE. It was lightweight, easy to use, and applications could be deployed in a web container (such as Tomcat) instead of a heavy J2EE application server. Deployment took seconds instead of 15 minutes. Unfortunately, JRebel did not exist at that time. The Spring framework is no standard as J2EE, nevertheless it became very widespread and an large community arose.

Today: J2EE is dead. JEE „stole“ the lightweight Spring ideas!
--------------------------------------------------------------
Everything started with a little shortcut change. J2EE was dead. The new shortcut was JEE. JEE 5 was born in 2006. It „stole“ many good, lightweight ideas such as „convention over configuration“ or „dependency injection“ from Spring and other frameworks. Yes, JEE application servers still were heavy, and testing was almost impossible. Nevertheless, developing JEE applications was fun with JEE 5. You did not have to write 20 interfaces when creating an EJB. Wow, amazing!

Then, in 2009, JEE 6 was released. Development is so easy. Finally! For example, you have to add only one annotation and your EJB is ready! Of course, the developers of the Spring framework did not sleep. Much new stuff was added. Today, you can create a Spring application without any one XML file as I have read in a „No Fluff Just Stuff“ article some weeks ago. Besides, several really cool frameworks were added to the Spring stack, e.g. Spring Integration, Spring Batch or Spring Roo.
Today (November, 2011), both JEE and Spring are very widespread and have a large community. Much information is available for both, e.g. books, blogs, tutorials, etc.
So, after I have described the evolution of JEE and Spring, why will I use JEE in most new Java projects?

Pros and Cons of JEE and Spring
--------------------------------
A decision must be made. Which alternative to use in new projects? Let’s look at the pros and cons of both. I will add a „BUT“ to the Spring advantages – these „BUTs“ are the reason why I prefer JEE to Spring.

Advantages of JEE
-----------------
    JEE is a set of standard specifications, thus it is vendor-independent. Usually, several implementations exist of a specification.
    Sustainability: Well, this is the advantage of a standard which is supported by several big players.
    Yes, believe it or not, testing is possible! Lightweight application servers and frameworks such as Arquillian arrived in the JEE world!
    Convention over Configuration is everywhere instead of explicit (I know that some people will disagree that this is an advantage).

Advantages of Spring
--------------------
    You do not need a heavy JEE application server, you can deploy your application in a web container such as Tomcat.
	
---------------------------------------------------------------------------------------------------------------------------------------------
(20) EXTJS
----------
<link rel="stylesheet" type="text/css"  href="ext-all.css" />
<script src="ext-all.js"></script>
<script src="apps.js"></script>
Model
View
Controller
Stores - Store has array of models
Resources

The Application contains global settings for your application 
Ext.Application(
{
name:'MyApp',
models:['model1','model2'],
stores:['store1','store2'],
views:['views1','views2'],
requires:['MyApp.view.views1'],
autoCreateViewPort:true
}
);


			Extends
Model  - Ext.data.Model	-	Ext.define('MyApp.model.model1',{extends:'Ext.data.Model',fields:[{name:'Column1',type:'string'},{name:'Column2'}]});

fields contains
---------------
fields:[
	{
	name:'',
	type:[],
	model:
	}
]


Stores - Ext.data.Store	-	Ext.define('MyApp.Store.Store1',{extends:'Ext.data.Store', requires:['MyApp.model.model1'],belongsTo:'modelN'});
View   - Ext.panel.Panel-	Ext.define();

Ext.define('MyApp.model.DeliveryDetailModel', {
    extend: 'Ext.data.Model',
    fields: [
        {name: 'deliveryModelName'},
        {name: 'deliveryMethod'},
		{name:'deliveryFileSpec'},
		{name: 'sourceCF'},
		{name:'outputFileType'},
		{name: 'delimiter'},
		{name: 'outputFileName'},
		
		{name: 'subscribers',
			model: 'SubscriptionsListModel',
			type: []
        },
		
		{name: 'deliverySpec',
			model: 'DeliverySpecModel',
			type: []
        }
    ]
});

Ext.define('MyApp.model.SubscriptionsListModel', {
    extend: 'Ext.data.Model',
    fields: [
        {
            name: 'modelName'
        }
	],
	belongsTo: 'DeliveryDetailModel'
});

Ext.define('MyApp.model.DeliverySpecModel', {
    extend: 'Ext.data.Model',
    fields: [
        {
            name: 'sourceField'
        },
		{
            name: 'targetField'
        },
		{
            name: 'dataType'
        }
	],
	belongsTo: 'DeliveryDetailModel'
});

(20.a) JavaScript
------------------
<script>
if(top!=self)
top.location = self.location;
</script
---------------------------------------------------------------------------------------------------------------------------------------------
(21) Learn Hibernate
--------------------
1.) Add Hibernate library to your project
2.) Oracle JDBC dirver library
3.) In Eclipse Install New Software specify update site of hibernate which is eclipse version specific
hibernate - http://download.jboss.org/jbosstools/updates/stable/juno
check only hibernate tool under every features
install these plugins and restart eclipse.
4.) Choose Hibernate prespective
5.) Add hibernate.cfg.xml & hibernate.properties files to your project
	and mention all required connection properties to the database.
6.) Go to File -> New -> Hibernate Console Configuration.
7.) Create a new database connection over here and provide hibernate.cfg.xml & hibernate.properties file
	7.1) When creating new db connection, select driver properties and choose new driver template
	7.2) Here SID of your DB can be get from "select sys_context('userenv','instance_name') from dual;"
8.) This will fetch all the table in particular schema (If this takes time, stop and create reveng.xml manually)
9.) Create a "hibernate.reveng.xml"	 in your project path.
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE hibernate-reverse-engineering PUBLIC "-//Hibernate/Hibernate Reverse Engineering DTD 3.0//EN" "http://hibernate.sourceforge.net/hibernate-reverse-engineering-3.0.dtd" >
<hibernate-reverse-engineering>
  <table-filter match-schema="BKMAIN" match-name="DIM_ACCOUNT"/>
  <table-filter match-schema="BKMAIN" match-name="DIM_COUNTRY"/>
</hibernate-reverse-engineering>
10.) Go to File -> New -> Hibernate Reverse engineering file
11.) Select reveng.xml in the opening window.
12.) RUN AS Hibernate code generation configurations.
13.) provide required information and select the required files to generate from database click on RUN 
13.a) information to provide are output directory, revenge xml location. Under Export tab check Generate EJB3 annotations and files needs to be generated.

	

How to generate hibernate mapping file i.e., 
1) TableName.hbm.xml
 http://sourceforge.net/projects/hibernate/files/hibernate4/.
 http://examples.javacodegeeks.com/enterprise-java/hibernate/hibernate-jboss-tools-installation-in-eclipse-mapping-generation-example/
http://www.javacodegeeks.com/2013/10/step-by-step-auto-code-generation-for-pojo-domain-java-classes-and-hbm-using-eclipse-hibernate-plugin.html

hibernate.cfg.xml
-----------------
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE hibernate-configuration PUBLIC"-//Hibernate/Hibernate Configuration DTD 3.0//EN""http://hibernate.sourceforge.net/hibernate-configuration-3.0.dtd">
<hibernate-configuration>
    <session-factory>
        <property name="hibernate.connection.driver_class">oracle.jdbc.driver.OracleDriver</property>
        <property name="hibernate.connection.url">jdbc:oracle:thin:@127.0.0.1:1521:MKYONG</property>
        <property name="hibernate.connection.username">mkyong</property>
        <property name="hibernate.connection.password">password</property>
        <property name="hibernate.dialect">org.hibernate.dialect.Oracle10gDialect</property>
        <property name="hibernate.default_schema">MKYONG</property>
        <property name="show_sql">true</property>
        <mapping class="com.bnymellon.eri.mmisettlements.model.DimCustomer"></mapping>
        <mapping resource="com/mkyong/user/DBUser.hbm.xml"></mapping>
    </session-factory>
</hibernate-configuration>

DBUser.hbm.xml
--------------
<?xml version="1.0"?>
<!DOCTYPE hibernate-mapping PUBLIC "-//Hibernate/Hibernate Mapping DTD 3.0//EN"
"http://hibernate.sourceforge.net/hibernate-mapping-3.0.dtd">
<hibernate-mapping>
	<class name="com.mkyong.user.DBUser" table="DBUSER">
		<id name="userId" type="int">
			<column name="USER_ID" precision="5" scale="0" />
			<generator class="assigned" />
		</id>
		<property name="username" type="string">
			<column name="USERNAME" length="20" not-null="true" />
		</property>
		<property name="createdBy" type="string">
			<column name="CREATED_BY" length="20" not-null="true" />
		</property>
		<property name="createdDate" type="date">
			<column name="CREATED_DATE" length="7" not-null="true" />
		</property>
	</class>
</hibernate-mapping>

HIBERNATE CALL
--------------
import org.hibernate.Session;
import com.mkyong.util.HibernateUtil;
import com.mkyong.user.DBUser;
public class App {
	public static void main(String[] args) {
		
		Session session = HibernateUtil.getSessionFactory().openSession();

		session.beginTransaction();
		DBUser user = new DBUser();

		user.setUserId(100);
		user.setUsername("superman");
		user.setCreatedBy("system");
		user.setCreatedDate(new Date());

		session.save(user);
		session.getTransaction().commit();
	}
}


package com.mkyong.util;

import org.hibernate.SessionFactory;
import org.hibernate.cfg.Configuration;

public class HibernateUtil {

	private static final SessionFactory sessionFactory = buildSessionFactory();

	private static SessionFactory buildSessionFactory() {
		try {
			// Create the SessionFactory from hibernate.cfg.xml
			return new Configuration().configure().buildSessionFactory();
		} catch (Throwable ex) {
			// Make sure you log the exception, as it might be swallowed
			System.err.println("Initial SessionFactory creation failed." + ex);
			throw new ExceptionInInitializerError(ex);
		}
	}

	public static SessionFactory getSessionFactory() {
		return sessionFactory;
	}

	public static void shutdown() {
		// Close caches and connection pools
		getSessionFactory().close();
	}

}


(21.a) DTO Vs DAO
-----------------
The DTO/DAO would be your model in the MVC pattern

DAO is a class that usually has the CRUD operations like save, update, delete. Whereas the DTO is just an object that holds data. It is really a glorified JavaBean with instance variables and setter and getters. Usually it is the DTO that is passed to the save method of a DAO.

Data Access Object (DAO) -> CRUD Operations
Data Transfer Object (DTO) -> getter & setter properties

Ref: http://howtodoinjava.com/2013/03/21/spring-3-and-hibernate-integration-tutorial-with-example/
---------------------------------------------------------------------------------------------------------------------------------------------
(23) Java webservice
---------------------------------------------------------------------------------------------------------------------------------------------
There are two ways to develop a web service namely top-down approach and bottom-up approach.

Bottom Up Approach

Bottom up approach is where we first define the logic of a web service and then using that we will build the interface. Service code is written first and then the WSDL is created using the service code. There are tools available to generate the wsdl file automatically based on it.

Top Down Approach

Top down is the reverse of bottom up approach. First the service definition is written up. WSDL is created first. The complete service definition, message format, transport protocol, security and everything is described in WSDL. Then service is written after the WSDL. Using that wsdl the skeleton code is generated automatically and after that the service code is filled up.

Stateless vs Statefull
----------------------
Web services are by nature stateless. Any attempt to maintain state is a hack, since you may hold something that will be used by the next request from the user, which will never come. Services should be stateless; if there's state to be maintained, it's the client's job to do it.

If you really need it, just keep it in session. For larger data sets, keep them out of session, but add session listener to cleanup that data when session expires.


Eclipse by default uses Apache Axis to implement the web service and it provides option to use our choice of web service engine.

1.) JAX-WS
SOAP (communication protocal) + HTTP
This is one of the possible forms of RPC (remote procedure call) architecture style. In essence, it's just a technology that allows clients call methods of server via service boundaries (network, processes, etc) as if they were calling local methods. Of course, it actually differs from calling local methods in speed, reliability and so on, but the idea is that simple.

SOAP defines a standard communication protocol (set of rules) specification for XML-based message exchange. SOAP uses different transport protocols, such as HTTP and SMTP. The standard protocol HTTP makes it easier for SOAP model to tunnel across firewalls and proxies without any modifications to the SOAP protocol. SOAP can sometimes be slower than middleware technologies like CORBA or ICE due to its verbose XML format.

WSDL (Web service description Language)  
WSDL is a XML based interface , that describes functionalities offered by web service
It covers all the aspects of a web service like what is the message format, communication protocol, endpoint, security etc

UDDI (Universal Description Discovery & Integration)  - is a directory service. Web services can register with a UDDI and make themselves available through it for discovery. It is like a marriage broker :-) People ready to get married will describe themselves in a standard format (WSDL) and register with this directory. People seeking pair will approach this directory and discover based on the information provided and approach.

Endpoint - An endpoint is a particular network location with associated protocol which includes message format mapping using which we can access that instance of web service. This is described in WSDL file. Consider this as a handle using which we will access the web service.


2.) Java API for RESTful Services (JAX-RS) Representational State Transfer (REST) 
simply explained : JAX-RS: Java API for RESTful Web Services (JAX-RS) is a Java programming language API spec that provides support in creating web services according to the Representational State Transfer (REST) architectural pattern

JAX-RS Implementation list
--------------------------
Apache CXF
Jersey from sun
RESTeasy from JBoss
Restlet
Everrest
jello-Framework

web.xml
  <servlet>
  <servlet-name>DispatcherServlet</servlet-name>
  <servlet-class>org.glassfish.jersey.servlet.ServletContainer</servlet-class>
  <init-param>
  <param-name>jersey.config.server.provider.packages</param-name>
  <param-value>emp</param-value>
  </init-param>
  <load-on-startup>1</load-on-startup>
  </servlet>
  
  <servlet-mapping>
  <servlet-name>DispatcherServlet</servlet-name>
  <url-pattern>/api/*</url-pattern>
  </servlet-mapping>
  
  package emp;

import javax.ws.rs.GET;
import javax.ws.rs.Path;
import javax.ws.rs.Produces;
import javax.ws.rs.core.MediaType;

@Path("/empapi")
public class Emp {

	@GET
	@Produces(MediaType.TEXT_HTML)
	public String greetEmp() {
		return "<h1>Hello emp</h1>";
	}
}

If you are using spring {WebApplicationInitializer} (SPI), which is detected/bootstrapped atomatically by  {SpringServletContainerInitializer}

public class webInitializer implements WebApplicationInitializer{
@Override
public void onStartup(ServletContext servletContext) throws ServletException{
}
}

3.) StAX (Streaming API for XML)
StAX enables you to create bidrectional XML parsers that are fast, relatively easy to program, and have a light memory footprint.

The Java Architecture/API for XML Web Services (JAX-WS)
The Java Architecture/API for XML Binding (JAXB)
The StAX APIs and the Sun Java Streaming XML Parser implementation
SOAP with Attachments API for Java (SAAJ)
The Java Architecture/API for XML Registries
XML Digital Signature
Security in the Web Tier


REST vs. SOAP

Multiple factors need to be considered when choosing a particular type of Web service, that is between REST and SOAP. The table below breaks down the features of each Web service based on personal experience.

REST

    The RESTful Web services are completely stateless. This can be tested by restarting the server and checking if the interactions are able to survive.
    Restful services provide a good caching infrastructure over HTTP GET method (for most servers). This can improve the performance, if the data the Web service returns is not altered frequently and not dynamic in nature.
    The service producer and service consumer need to have a common understanding of the context as well as the content being passed along as there is no standard set of rules to describe the REST Web services interface.
    REST is particularly useful for restricted-profile devices such as mobile and PDAs for which the overhead of additional parameters like headers and other SOAP elements are less.
    REST services are easy to integrate with the existing websites and are exposed with XML so the HTML pages can consume the same with ease. There is hardly any need to refactor the existing website architecture. This makes developers more productive and comfortable as they will not have to rewrite everything from scratch and just need to add on the existing functionality.
    REST-based implementation is simple compared to SOAP.

SOAP

    The Web Services Description Language (WSDL) contains and describes the common set of rules to define the messages, bindings, operations and location of the Web service. WSDL is a sort of formal contract to define the interface that the Web service offers.
    SOAP requires less plumbing code than REST services design, (i.e., transactions, security, coordination, addressing, trust, etc.) Most real-world applications are not simple and support complex operations, which require conversational state and contextual information to be maintained. With the SOAP approach, developers need not worry about writing this plumbing code into the application layer themselves.
    SOAP Web services (such as JAX-WS) are useful in handling asynchronous processing and invocation.
    SOAP supports several protocols and technologies, including WSDL, XSDs, SOAP, WS-Addressing

In a nutshell, when you're publishing a complex application program interface (API) to the outside world, SOAP will be more useful. But when something with a lower learning curve, and with lightweight and faster results and simple transactions (i.e., CRUD operations) is needed, my vote goes to REST.
Invoking Web service via Oracle database stored procedure

Consuming a Web service via a database stored procedure allows users to straight away update a database with information from different sources. Users can also schedule a job at regular intervals to get data updated periodically in the database. 

Oracle provides a "utl_http" utility to help achieve this. Below is sample code for the Oracle package for a customer where the Web service call is made from the database.
--------------------------------------------------------------
example
-------
Base class used is import javax.jws.WebService;

package helloservice.endpoint;
import javax.jws.WebService;
@WebService
public class Hello {
    private String message = new String("Hello, ");

    public void Hello() {}

    @WebMethod
    public String sayHello(String name) {
        return message + name + ".";
    }
}

package simpleclient;

import javax.xml.ws.WebServiceRef;
import helloservice.endpoint.HelloService;
import helloservice.endpoint.Hello;

public class HelloClient {
    @WebServiceRef(wsdlLocation="http://localhost:8080/
            helloservice/hello?wsdl")
    static HelloService service;

    public static void main(String[] args) {
        try {
            HelloClient client = new HelloClient();
            client.doTest(args);
        } catch(Exception e) {
            e.printStackTrace();
        }
    }

    public void doTest(String[] args) {
        try {
            System.out.println("Retrieving the port from
                     the following service: " + service);
            Hello port = service.getHelloPort();
            System.out.println("Invoking the sayHello operation
                     on the port.");

            String name;
            if (args.length > 0) {
                name = args[0];
            } else {
                name = "No Name";
            }

            String response = port.sayHello(name);
            System.out.println(response);
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}

---------------------------------------------------------------------------------------------------------------------------------------------
(24) EJB
---------------------------------------------------------------------------------------------------------------------------------------------
Enterprise Java Beans: There are three types of EJBs. They are

 Session Beans,
 Entity Beans, and
 Message-Driven Beans

---------------------------------------------------------------------------------------------------------------------------------------------
(25) Drools (Rules engine)
---------------------------------------------------------------------------------------------------------------------------------------------
 A Decision service REST API. Requires JBOSS rules engine library. It can be configured by adding a properties file that provides the location of our rules file.
 We have spoken often of the necessity of separating business rules from business process. For those new to business rules, consider two points:

• The need to manage business rules independently from the process: Business rules tend to change more frequently than does business process. When rules are embedded in process, changes are significantly more difficult to execute than when they are managed in a Business Rules Management System (BRMS).

• Single point of maintenance: A business rule may be used in many different processes, and/or at several points in a single process. By maintaining business rules in a BRMS, the change may be made once, and sometimes simply by a business analyst.
---------------------------------------------------------------------------------------------------------------------------------------------
(26) 
---------------------------------------------------------------------------------------------------------------------------------------------

---------------------------------------------------------------------------------------------------------------------------------------------
(27) API vs SPI
the API is the description of classes/interfaces/methods/... that you call and use to achieve a goal and
the SPI is the description of classes/interfaces/methods/... that you extend and implement to achieve a goal
---------------------------------------------------------------------------------------------------------------------------------------------
 
---------------------------------------------------------------------------------------------------------------------------------------------
Achievement
---------------------------------------------------------------------------------------------------------------------------------------------
A1) Tomcat installation
-----------------------
either you can set a environment variable

C:\>set CATALINA_HOME=C:\software\tomcat-5.0.28  
C:\>%CATALINA_HOME%\bin\startup.bat  

OR

Inside Tomcat folder and execute startup.bat

if port of tomcat has to be changed then just locate server.xml file and replace 8080 to 80

then navigate to http://localhost:80 to launch tomcate server

A2) Reading CSV file
---------------------

A3) Reading a #.doc file and parsing it
---------------------------------------

A4) Writing into EXCEL File
---------------------------

----------------------------------------------------------------------------------------------------------------------------------------------
ERROR
---------------------------------------------------------------------------------------------------------------------------------------------

1.) could not find main class while executing the JAR 
C:\>java -cp "C:\<your file location>\FileLayoutDocParser.jar" bnym.eri.tf.filelayoutparser.FileLayoutParserUI

2.) NullPointerException when modify JComboBox when there are event listener binded
solution : remove required event listener, modify JComboBox item as required and append required event listener

3>0 
----------------------------------------------------------------------------------------------------------------------------------------------
SVN
---



http://rk6qn0c/OBIEEWebService/services/ReportServicePort?wsdl

----------------------------------------------------------------------------------------------------------------------------------------------
(26) nodejs
------
Node.js is an open source command line tool built for the server side JavaScript code
Node.js (Node) is an I/O environment built on top of Google Chrome's JavaScript runtime — essentially, a server-side implementation of JavaScript. Node's asynchronous, event-driven I/O model makes it easy for developers with JavaScript knowledge to build high-performing, scalable, and highly concurrent web applications rapidly and run them in the cloud.
Event-driven architecture (EDA)
An event can be defined as, a significant change in state

For example, when a consumer purchases a car, the car's state changes from "for sale" to "sold". A car dealer's system architecture may treat this state change as an event whose 
occurrence can be made known to other applications within the architecture. From a formal perspective, what is produced, published, propagated, detected or consumed is a (
typically asynchronous) message called the event notification, and not the event itself, which is the state change that triggered the message emission. Events do not travel, 
they just occur. However, the term event is often used metonymically to denote the notification message itself, which may lead to some confusion.

The V8 JavaScript Engine 
------------------------
It is an open source JavaScript engine developed by Google for the Google Chrome web browser.
V8 compiles JavaScript to native machine code before executing it, instead of more traditional techniques such as interpreting bytecode or compiling the whole program to machine code and executing it from a filesystem.

usecase
-------
The chat application is really the sweet-spot example for Node.js: it’s a lightweight, high traffic, data-intensive (but low processing/computation) application that runs across distributed devices. It’s also a great use-case for learning too, as it’s simple,

Why use Node?
-----------
1.) Firstly, for performance and scalability.
2.) Node site will never lock up and can support tens of thousands of concurrent users
3.) multithreaded approach with single-threaded, event-driven I/O
4.) It was created to solve the I/O scaling problem, which it does really well

Downside, Cons
--------
1.) It’s also important to note that Node is not simply a replacement for Apache – existing web applications are not compatible, and you’ll be working effectively from scratch (though there are a lot of frameworks out there to help you with common features).  The other major downside to node is that it’s still in the early stages of development, meaning some features are likely to change as development progresses. In fact, if you look at the documentation, it includes a stability index, which shows how risky use of each feature is currently. 
2.) heavy computation could choke up Node’s single thread and cause problems for all clients (more on this later) as incoming requests would be blocked until said computation was completed.
3.) Using Node.js with a relational database is still quite a pain
ref: http://www.toptal.com/nodejs/why-the-hell-would-i-use-node-js
--------------------------------------------------------------------------------------------------------------------------------------------------------
27) ExecutorService Future

1.) execute(Runnable. void Run())
2.) future = Submit(Runnable.void Run()); future.get();
3.) future = Submit(Callable. Object Call()); future.get();
4.) execService.ShutDown() //no more taks can be added
5.) execService.ShutDownnow() //stops immidiately and returns pending task 
6.) execService.awaitTermination() // awaite untill all thread added to pool get completed


execute(Runnable)
-----------------
The execute(Runnable) method takes a java.lang.Runnable object, and executes it asynchronously. Here is an example of executing a Runnable with an ExecutorService:

ExecutorService executorService = Executors.newSingleThreadExecutor();

executorService.execute(new Runnable() {
    public void run() {
        System.out.println("Asynchronous task");
    }
});

executorService.shutdown();
There is no way of obtaining the result of the executed Runnable, if necessary. You will have to use a Callable for that (explained in the following sections).


submit(Runnable)
----------------
The submit(Runnable) method also takes a Runnable implementation, but returns a Future object. This Future object can be used to check if the Runnable as finished executing.

Here is a ExecutorService submit() example:

Future future = executorService.submit(new Runnable() {
    public void run() {
        System.out.println("Asynchronous task");
    }
});

future.get();  //returns null if the task has finished correctly.

submit(Callable)
----------------
The submit(Callable) method is similar to the submit(Runnable) method except for the type of parameter it takes. The Callable instance is very similar to a Runnable except that its call() method can return a result. The Runnable.run() method cannot return a result.

The Callable's result can be obtained via the Future object returned by the submit(Callable) method. Here is an ExecutorService Callable example:

Future future = executorService.submit(new Callable(){
    public Object call() throws Exception {
        System.out.println("Asynchronous Callable");
        return "Callable Result";
    }
});

System.out.println("future.get() = " + future.get());
The above code example will output this:

Asynchronous Callable
future.get() = Callable Result


Identify which thread is currently running
-------------------------------------------
 public void run() {
        System.out.println(Thread.currentThread().getName()+" Start. Command = "+command);
        processCommand();
        System.out.println(Thread.currentThread().getName()+" End.");
    }
	
	
	
----------------------------------------------------------
	SEVERE: A child container failed during start
	
---------------------------------------------------------------------------------------------------------	
(28) collection Set/List/Queue/Map : 

Remember
# Collection does not hold premitive types {int, flot, double, byte, char, bollean} (stored in Stack) int i1 = i;{UnBoxing}
# Collection can hold Non-premitive types {Integer, Double, Boolean, String} (Storead on heap) Integer i = 32 {Boxing}
# Hash never support order, so unordered
# Linked maintain order of insertion
# Being an interface means it cannot be instantiated (so List<T> lst=new List() is not possible)
following is possible bcz ArrayList is class that 
List<String> supplierNames = new ArrayList<String>(); 

Collection is an interface extends Iterable

interface Set extends Collection does not allow duplicates
interface SortedSet extends set
interface NavigableSet extends SortedSet
Class TreeSet implements Set & NavigableSet
Class LinkedHashSet implements set

interface List extends Collection allows duplicates
Array fixed size
ArrayList implements List (can grow and shrink)


interface Queue extends Collection, process orderly manner {add/offer/remove/poll/peek}
interface Deque extends Queue, {add either first/last, offer either first/last, poll either first/last}
interface BlockingQueue extends Queue (based on time) {add/offer/remove/poll}
Class PriorityQueue
Class ArrayDqueue
Class ArrayBlockingQueue
Class LinkedBlockingQueue


Map <K,V> key is a unique identifier & does not extend Collection
interface SortedMap<K,V> extends Map<K,V>
interface NavigableMap<K,V> key> key< key=
class HashMap<K,V> Unsorted Unordered
class HashTable<K,V> Synchronized
class LinkedHashMap<K, V> insertion order is maintained 
class TreeMap implements Map & Navigable

ArrayList Vs LinkedList
Implements List
Insertion & deletion in ArrayList is slower than Linked List
ArrayList is not Thread Safe

LinkedList
Implements List  & Queue
Fast insertion & deletion

Vector (Syncronized)
Thread Safe
---------------------------------------------------------------------------------------------------------	
