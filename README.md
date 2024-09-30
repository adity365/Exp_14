# Experiment 14

## Inheritance 
In general programming, **inheritance** is a concept where one class (called a subclass or derived class) inherits the properties and behaviors (methods) of another class (called a superclass or base class). In OOP, the types of inheritance are:

1. **Single Inheritance**: A subclass inherits from one superclass.
   
2. **Multiple Inheritance**: A subclass inherits from more than one superclass.
   
3. **Multilevel Inheritance**: A subclass inherits from a class that itself inherits from another class.
   
4. **Hierarchical Inheritance**: Multiple subclasses inherit from a single superclass.
   
5. **Hybrid Inheritance**: A combination of two or more types of inheritance (e.g., multiple and multilevel).

These types help create a structured and reusable class hierarchy in object-oriented programming.

Experiment 14(a)

```// Name --> Aditya Agarwal
// PRN --> 23070123162

// What is Inheritance ??
// Inheritance in c++ is a fundamental concept in oops that allow one class(child class) to inherit the properties and behavior(meathods) from parent class 
// This promotes code reuse and a hierarchical class structure.

// Code which demonstrate Single level Inheritance

# include <iostream>
# include <string>
using namespace std;

//single inheritance
class uni // Parent Class
{
    public:
    string uni = "Symbiosis";
    void course()
    {
        cout<<"B. Tech ";
    }
};
class branch/*child class*/: public uni 
// by this, the child class gets inherits the properties of the parent class
// and Electronics and telecommunication also gets printed along with B. Tech.
{
    public:
    string branch = " Electronics and Telecommunication ";

};

int main()
{
    branch b1;
    cout<<b1.uni<<endl;
    b1.course();
    cout<<b1.branch;
}
```
Experiment 14 (b)
```
// Name --> Aditya Agarwal
// PRN --> 23070123162

// Code which demonstrates Multiple Inhertance 
// Multiple Inheritance -> A derived class inherits from more than one base class.
# include <iostream>
# include <string>
using namespace std;

//multiple inheritance
class mammal // child class 1
{
    public:
    string mammal = "Kingdom Mammalia";
    void exp()
    {
        cout<<"Exceptions: ";
    }
};
class aquatic // child class 2
{
    public:
    string aqua = "Species living in the water ";

};

class walrus:public aquatic,public mammal // joining both child class 1 and 2

// Derived class has access to meathods from both aquatic and mammal
{
    public:
    string wallie = "Walrus are mammals which are aquatic ";

};
int main()
{
    walrus b1;
    cout<<b1.mammal<<endl;
    b1.exp();
    cout<<b1.wallie;
}

```
Experiment 14(c)
```
// Name --> Aditya Agarwal
// PRN --> 23070123162

// Code which demonstrates Multilevel Inheritance 
// Multilevel Inheritance -> A class is derived from a class which is already derieved from another class.

# include <iostream>
# include <string>
using namespace std;

//multilevel inheritance
class kingdom
{
    public:
    string hum = "Human Classification";
    void king()
    {
        cout<<"Kingdom: Animalia ";
    }
};
class phylum: public kingdom
{
    public:
    string phy = "Phylum: Cordata ";

};

class classs:public phylum
{
    public:
    string cla = "Class: Mammalia ";

};
class order:public classs
{
    public:
    string ord = "Order: Primates ";

};
class family:public order
{
    public:
    string fam = "Family: Homonidae";

};
class genus:public family
{
    public:
    string gen = "Genus: Homo";

};
class species:public genus
{
    public:
    string spe = "Species: Species";

};
int main()
{
    species h1;
    cout<<h1.hum<<endl;
    h1.king();
    cout<<endl;
    cout<<h1.phy<<endl;
    cout<<h1.cla<<endl;
    cout<<h1.ord<<endl;
    cout<<h1.fam<<endl;
    cout<<h1.gen<<endl;
    cout<<h1.spe<<endl;


}
```
Experiment 14(d)
```
// Name --> Aditya Agarwal
// PRN --> 23070123162

// Code which demonstrates Hierarchical Inheritance 
// Hierarchical Inheritance -> Multiple classes inherit form a single base class.
# include <iostream>
# include <string>
using namespace std;

//hierarchical inheritance
class fivekingdom
{
    public:
    string fiv = " is one of the kingdoms in the 5 Kingdom Classification";

};
class animalia: public fivekingdom
{
    public:
    string ani = "Animalia";

};
class monera: public fivekingdom
{
    public:
    string mon = "Monera";

};
class protists: public fivekingdom
{
    public:
    string pro = "Protists";

};
class fungi: public fivekingdom
{
    public:
    string fun = "Fungi";

};
class plantae: public fivekingdom
{
    public:
    string pla = "Plantea";

};
int main()
{
    animalia k1;
    monera k2;
    protists k3;
    fungi k4;
    plantae k5;

    
    cout<<k1.ani;
    cout<<k1.fiv<<endl;

    cout<<k2.mon;
    cout<<k1.fiv<<endl;

    cout<<k3.pro;
    cout<<k1.fiv<<endl;

    cout<<k4.fun;
    cout<<k1.fiv<<endl;
    
    cout<<k5.pla;
    cout<<k1.fiv<<endl;


}

```
