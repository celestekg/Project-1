# Project-1: This program calcuates the day of the week for any date entered, and prints the result.

![image](https://user-images.githubusercontent.com/56613527/162595019-defd2dfc-45b6-44aa-82b8-86adb700046d.png)

#include <iostream>
#include <cstdlib>
#include <string>

using namespace std;

int main()
{
	int m;
	int q;
	int j;
	int k;
	int h;
	string wordDay;

	cout << "Enter month (1-12): ";
	cin >> m;

	cout << "Enter day (1-31): ";
	cin >> q;

	cout << "Enter century: ";
	cin >> j;

	cout << "Enter year of the century: ";
	cin >> k;

	h = (q + ((26 * (m + 1)) / 10) + k + (k / 4) +(j / 4) + (5 * j)) % 7;

	switch (h)
	{

	case 0:
		wordDay = "Saturday";
		break;

	case 1:
		wordDay = "Sunday";
		break;

	case 2:
		wordDay = "Monday";
		break;

	case 3:
		wordDay = "Tuesday";
		break;

	case 4:
		wordDay = "Wednesday";
		break;

	case 5:
		wordDay = "Thursday";
		break;

	case 6:
		wordDay = "Friday";
		break;
	}

	cout << "The day of the week is " << h << " (" << wordDay << ")" << endl;
	system("PAUSE");
	return 0;
}
