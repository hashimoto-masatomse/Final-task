# Final-task
Repository of final task

#include <iostream>
#include <math.h>
#include <vector>
#include <algorithm>
using namespace std;

class Houteisiki {
public:
	void f() {
		vector<float> v; //２次方程式の解を格納するvector

		cout << "aを入力してください。\n";
		float a;
		cin >> a;
		cout << "bを入力してください。\n";
		float b;
		cin >> b;
		cout << "cを入力してください。\n";
		float c;
		cin >> c;

		float D; //判別式
		float x, y; //２次方程式の解

		D = b * b - 4 * a * c; //判別式の計算

		//for (int i = 0; i < 2; ++i) { //判別式の数値により場合分け
			if (D > 0) {
				x = (-b + sqrt(D)) / (2 * a);
				y = (-b - sqrt(D)) / (2 * a);
				v.push_back(x);
				v.push_back(y);
				cout << "t=" << v[0] << "," << v[1]; //２次方程式の解
			}
			else if (D == 0) {
				x = y = -b / (2 * a);
				v.push_back(x);
				v.push_back(y);
				cout << "t=" << v[0] << "," << v[1]; //２次方程式の解
			}
			else {
				cout << "t=" << "複素数解" << "," << "複素数解"; //２次方程式の解
			}
		//}
		cout << endl;

		cout << "それらを昇順にすると\n";
		vector<float> v1 = v;

		sort(v1.begin(), v1.end());
		for (auto n : v1)
			cout << n << ",";
		cout << endl;
	}
};

int main(vector<float> v) {
	Houteisiki siki;
	siki.f();
}
