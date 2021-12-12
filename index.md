# Report of const and & 
## the usage of const in c++
### const for declaring variables 
- fix thier memory at compile time and donot change during run time
- as ex: 
````
```
const int a =5;
```
````
- the size of the static array is constant by default// example of const values
### const for declare pointer 
- this pointer points to const variable
- as ex :
````
```
const int* u;\\ pointsto const int variable
```
````
### const member function
- this makes function read only
- and const keyworld is required in both declaration and the definition.
- example:
````
```
class Date
```
{
public:
   Date( int mn, int dy, int yr );
   
   int getMonth() const;  
   // A read-only function
   void setMonth( int mn );
   
   // A write function; can't be const
private:
   int month;
};
```
int Date::getMonth() const
{
   return month;      
   // Doesn't modify anything
}
void Date::setMonth( int mn )
{
   month = mn;        
   // Modifies data member
}

int main()
{
   Date MyDate( 7, 4, 1998 );
   
   const Date BirthDate( 1, 18, 1953 );
   
   MyDate.setMonth( 4 );  
   // Okay no error
   
   BirthDate.getMonth();   
   // Okay no error
   
   BirthDate.setMonth( 4 );
   // makes Error
}

```
````
### used in making constant class object 
- as ex:
````
```
const class_name my_object;
```
````
### const in class data member
````
```
class name {
const int a;
const string s;
}
```
````

## & usage
- get the address of variable to store it in a pointer
````
```
int a;
int*ptr =& a;
```
````
- used in methods by passing variable by refrence in the parameters
````
```
return_type function_name(&variable_name)//in this we can get the value returned from function to be stored in the refrence of the passed variable
```
````
- used as bitwise and that it compare each bit of the first operand to that bit of the second operand
````
```
 short a = 0x5555;
 short b = 0xAAAA;
cout<<(a&b);
```
````
- the symbol && means logical and
````
```
if(codition 1 && condition 2){
\\\do something
}
```
````
