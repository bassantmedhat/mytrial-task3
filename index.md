# Report of const and & 
## the usage of const in c++
### const for declaring variables 
- fix thier memory at compile time and donot change during run time
- as object_name.set(value)
--  this value is const parameter
- const size for static array
### const for declare pointer 
- this pointer points to const variable
-- as ex :const int* u;
### const member function
- this makes function read only
- and const keyworld is required in both declaration and the definition.
- as example
```
void f(const int i)
```
- another example:
```
class Date
{
public:
   Date( int mn, int dy, int yr );
   int getMonth() const;     // A read-only function
   void setMonth( int mn );   // A write function; can't be const
private:
   int month;
};

int Date::getMonth() const
{
   return month;        // Doesn't modify anything
}
void Date::setMonth( int mn )
{
   month = mn;          // Modifies data member
}
int main()
{
   Date MyDate( 7, 4, 1998 );
   const Date BirthDate( 1, 18, 1953 );
   MyDate.setMonth( 4 );    // Okay no error
   BirthDate.getMonth();    // Okay no error
   BirthDate.setMonth( 4 ); //   makes Error
}
```
### used in making class object constant
- as ex:
```
const class_name object;
```
## & usage
- get the value that the pointer points to
- get the address of variable to store it in pointer
- used in methods by passing variable by refrence in the parameters
- other name of the same thing 
- used as bitwise and that it compare each bit of the first operand to that bit of the second operand
- the symbol && means logical and
