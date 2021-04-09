#include<iostream>
using namespace std;

class calc {
private:
	int x;//операнд
public:
	calc() {
		x = 0;
	}
	calc(int xx) {
		x = xx;
	}
	void setx(int x) {//установить значение x
		this->x = x;
	}

	int getx() {//получить x
		return x;
	}

	friend ostream& operator<<(ostream& out, const calc& c)
	{
		out << c.x;
		return out;
	}
	friend istream& operator>>(istream& in, calc& c)
	{
		in >> c.x;
		return in;
	}
	calc operator++() {//оператор инкремента
		return calc(x++);
	}
	calc operator--() {//оператор декремента
		return calc(x--);
	}
	calc operator-(const calc& other) {//оператор минуса
		calc temp;
		temp.x = this->x - other.x;
		return temp;
	}

	calc operator+(const calc& other) {//оператор плюса
		calc temp;
		temp.x = this->x + other.x;
		return temp;
	}
	calc operator*(const calc& other) {//оператор умножения
		calc temp;
		temp.x = this->x * other.x;
		return temp;
	}
	calc operator/(const calc& other) {//оператор деления
		calc temp;
		temp.x = this->x / other.x;
		return temp;
	}
	bool operator==(const calc& right)
	{
		if (x == right.x)
			return true;
		else
			return false;
	}
	calc& operator=(const calc& right) {//оператор равенства
		if (this == &right) {
			return *this;
		}
		x = right.x;
		return *this;
	}
};


int main() {

	calc a;
	calc b;
	cin>>a;
	cin>> b;

	calc c;
	c = a + b;
	cout<<c<< endl;
	return 0;
}
