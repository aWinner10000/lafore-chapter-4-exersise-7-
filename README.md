/*Add a variable of type enum etype (see Exercise 6), and another variable of type struct
date (see Exercise 5) to the employee class of Exercise 4. Organize the resulting program so that the user enters four items of information for each of three employees: an
employee number, the employee’s compensation, the employee type, and the date of first
employment. The program should store this information in three variables of type
employee, and then display their contents#include <iostream>*/ 
#include <iomanip>
#include <CTYPE.H.>
#include <string>
#include <conio.h>
using namespace std;
// enum etype {secretary, manager, worker};
struct workdate {int day, month, year;};

struct employee {
int numb;
float salary;
workdate date;
enum post {secretary = 1, manager = 2, worker = 3} ;
};
int main()
{
       setlocale(LC_ALL, "Russian");
       employee one, two, three;
       int z, y;
       char x = '/';
       cout << " secretary 1, manager 2, worker 3 \n";
        cin >> z;
       switch (z) {
           case 1:
       cout << " for secretary :" << one.secretary << endl;
       cout << " numb "; cin >> one.numb;
       cout << " salary "; cin >> one.salary;
       cout << " workdate : "; cin >> one.date.day >> x >> one.date.month >> x >> one.date.year;
       break;
          case 2:
       cout << " for manager : " << two.manager << endl;
       cout << " numb "; cin >> two.numb;
       cout << " salary "; cin >> two.salary;
       cout << " workdate : "; cin >> two.date.day >> x >> two.date.month >> x >> two.date.year;
       break;
       case 3:
       cout << " for worker : " << three.worker << endl;
       cout << " numb "; cin >> three.numb;
       cout << " salary "; cin >> three.salary;
       cout << " workdate : "; cin >> three.date.day >> x >> three.date.month >> x >> three.date.year;
       break;
       default: cout << "error" ;
       //cout <<  " для рабочий : " <<  three.worker << endl;
       }
       if (z ==1 || z == 2 || z ==3) {
       cout << "out for secretary 1 manager 2 worker 3 \n";
       cin >> y;
       switch (y)
       {
       case 1:
        cout << " stare secretary :" << " numb " << one.numb
        << " salary  " << one.salary
        << " workdate " <<  one.date.day << "/" << one.date.month << "/" << one.date.year;
        break;
        case 2:
        cout << " state manager  :" << " numb " << two.numb
        << " salary  " << two.salary
        << " workdate " <<  two.date.day << "/" << two.date.month << "/" << two.date.year;
        break;
        case 3:
        cout << " state manager  :" << " numb " << three.numb
        << " salary  " << three.salary
        << " workdate " <<  three.date.day << "/" << three.date.month << "/" << three.date.year;
        break;
       }

                             }
                             else cout << "sorry ";

       return 0;
}
