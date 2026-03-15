Class defination:



	class <name\_class>{

		private:

			#Variables \& functions

		protected:

			#Variables \& functions
			
		public:

			#Variables \& functions

};



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





		ATTRIBUTES

Declaration: 

<type> <name\_attributes>

Notes:

* Like as common variables
* Mustn't set value for attributes in class. Attributes ONLY have value when it associated with a specific object



Using attributes:

* If it can be accessed from outside a class:

<class\_name>.<name\_attribute>;

* If using inside class:

<name\_attribute>;

NOTES: If name of attribute is same with global variable. We need to show exacly name attribute of the class. 

<class\_name>::<name\_attribute>;



		METHODS

Declaration:

<return\_type> <name\_method>(\[Parameters])

like as functions



Defination:

* Set inside class

<return\_type> <name\_method>(\[Parameters]){

	#Code

}



* Set outside:

<return\_type> <class\_name>::<name\_method>(\[Parametes]){

	#Code

}

NOTES:

* Parametes must be explicit
* Should defining method outside class (with methods have long implementation)



Using methods:

* If can be used outside class:

<class\_name>.<name\_method>(\[Parameters]);

* Use inside:

<name\_method>(\[Parameters]);



NOTES: When use a method in another method inside class, but method\_name duplicate with global function

<class\_name>::<name\_method>(\[Parameters]);





		SCOPE

blocks < functions < class < file





		FRIEND

Friend function: 

* free function 
* member method of one class that is a friend of another class



Free function



\#EXAMPLES:



class <class\_name>{

//Codes

//Declaring friend functions

friend <return\_type> <name\_method>(\[Parameters]);

};



<return\_type> <name\_method>(\[Parameters]){

//Can access directly private elements of class 

//that declares this method

}



NOTES:

* Friend functions are declared in class. However, that isn't methods of class -> Use like others free funtion.
* Can declare prototype friend function in anywher within the class scope (not affected by access modifiers)
* In friend function, members in private and protected of objects belong to class\_type that function is friend



Method in a class is friend of another class



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




