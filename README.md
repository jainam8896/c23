# c23#include<iostream.h>

#include<conio.h>

class person

{

	public:

	char name;

	int age;

	static person *eldest;

		person()

		{

			age=0;

			name='a';

		}

		person operator = (person &p)

		{

			person temp;

			temp.age=p.age;

			temp.name=p.name;

			return temp;

		}

		person(int a, char n)

		{

			age=a;

			name=n;

			if(person::eldest->age<a)

			{

				person::eldest->age=this->age;

				person::eldest->name=this->name;

			}

		}

};

person *person::eldest;

void main()

{

	clrscr();

	person p1(10,'p');

	person p2(8,'a');

	cout<<"Eldest Person Age: "<<person::eldest->age<<endl;

	cout<<"Eldest Person Name: "<<person::eldest->name<<endl;

	getch();

}
