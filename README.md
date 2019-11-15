# hello-world
# "Những năm tháng đó, tôi cái gì cũng có, chỉ có tiền là không có. Còn bây giờ, tôi cái gì cũng không có...kể cả tiền.".

#include <iostream>
#include <string>
#include <math.h>
using namespace std;
int main()
{
	cout << "Nhap dong thu nhat" << endl;
	int n;
	cin >> n;
	cin.ignore();
	cout << "Nhap dong thu hai " << endl;
	string str1;
	getline(cin, str1);
	string str2 = "";
	for (int i = 0; i < 2 * n; i++)
	{
		if (str1[i] >= '0' && str1[i] <= '9')
			str2 = str2 + str1[i];
	}
	int luythua = int(str2[n - 1]) - 48;
	for (int i = 1; i < n; i++)
	{
		luythua = pow(int(str2[n - i - 1]) - 48, luythua);
	}
	int ketQua = int(luythua) % 3;
	cout << ketQua << endl;
	return 0;
}
