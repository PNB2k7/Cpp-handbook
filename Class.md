Class defination:



&#x09;class <name\_class>{

&#x09;	private:

&#x09;		#Variables \& functions

&#x09;	protected:

&#x09;		#Variables \& functions

&#x09;	public:

&#x09;		#Variables \& functions

&#x09;};



NOTES:

* If don't set Access Modifiers (private, protected, public), systems implicits as private 
* <name\_class> should 1 upper letter at first, the others are lower letters



Access Modifiers

* private: all elements in that scope cannot be accessed from outside the class
* public: all elements in that scope can be accessed from outside the class
* protected: can set what can accessed from outside the class.





Elements in class can be divided into 2 groups:

* Attributes: variable or such thing that hold the data of a class (almost in private)
* Methods: function or similar elements that hold the action of a class (almost in public)





&#x09;		ATTRIBUTES

Declaration: 

&#x09;<type> <name\_attributes>

Notes:

* Like as common variables
* Mustn't set value for attributes in class. Attributes ONLY have value when it associated with a specific object



Using attributes:

* If it can be accessed from outside a class:

&#x09;<class\_name>.<name\_attribute>;

* If using inside class:

&#x09;<name\_attribute>;

NOTES: If name of attribute is same with global variable. We need to show exacly name attribute of the class. 

&#x09;<class\_name>::<name\_attribute>;



&#x09;		METHODS

Declaration:

&#x09;<return\_type> <name\_method>(\[Parameters])

like as functions



Defination:

* Set inside class

&#x09;<return\_type> <name\_method>(\[Parameters]){

&#x09;	#Code

&#x09;}



* Set outside:

&#x09;<return\_type> <class\_name>::<name\_method>(\[Parametes]){

&#x09;	#Code

&#x09;}

NOTES:

* Parametes must be explicit
* Should defining method outside class (with methods have long implementation)



Using methods:

* If can be used outside class:

&#x09;<class\_name>.<name\_method>(\[Parameters]);

* Use inside:

&#x09;<name\_method>(\[Parameters]);



NOTES: When use a method in another method inside class, but method\_name duplicate with global function

&#x09;<class\_name>::<name\_method>(\[Parameters]);





&#x09;		SCOPE

&#x09;blocks < functions < class < file





&#x09;		FRIEND

Friend function: 

* free function 
* member method of one class that is a friend of another class



&#x09;Free function



\#EXAMPLES:



class <class\_name>{

&#x09;//Codes

//Declaring friend functions

&#x09;friend <return\_type> <name\_method>(\[Parameters]);

};



<return\_type> <name\_method>(\[Parameters]){

&#x09;//Can access directly private elements of class 

&#x09;//that declares this method

}



NOTES:

* Friend functions are declared in class. However, that isn't methods of class -> Use like others free funtion.
* Can declare prototype friend function in anywher within the class scope (not affected by access modifiers)
* In friend function, members in private and protected of objects belong to class\_type that function is friend



&#x09;Method in a class is friend of another class



\#EXAMPLE



class A; //Declare prototype A to use as parameter for method in class B

class B{
	//Codes
	void f(A);
}

class A{
	friend void B::f(A);
};

void B::f(A){
	//Codes
}

NOTES:
- In this case, f is only defined when A has defined -> Mustn't define f inside B
- f can access into private protected of both class A,B. However, f want to access members in class A, f needs access through an object has A type.

		Friend class
All methods of a class is friend of another class -> friend class

#EXAMPLE
//Declare prototype class B
class B;

//Defining A with B is friend class;
class A{
	//Codes
	friend class B; //Declaring friend B
};

#Defining B
class B{
	//Codes
};

NOTES:
- In case, class B is friend A, but A don't have to friend B
- All methods in B can access member in class A (through an object has A type)




