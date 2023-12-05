#include <iostream>
#include <vector>
using namespace std;

//vars
bool cont = true;
vector<string> nameList;
vector<int> quantList;
vector<double> priceList;
//funcs

int main() {
	cout << "Welcome to checkout!" << endl;
	while (cont) {
		cout << "What is the next item's name?" << endl;
		string name;
		cin >> name;
		cout << "What is the item's price?" << endl;
		double unitPrice;
		cin >> unitPrice;
		cout << "What is the quantity?" << endl;
		int quant;
		cin >> quant;
		double totalPrice = unitPrice * quant;
		nameList.push_back(name);
		quantList.push_back(quant);
		priceList.push_back(totalPrice);
		cout << "Do you have any more items? (Y/N)" << endl;
		string contCheck;
		cin >> contCheck;
		if (contCheck == "Y") {
			cont = true;
		}
		else if (contCheck == "N") {
			cont = false;
		}
		else {
			cout << "The command was not understood, so the total price will be calculated anyway" << endl;
		}
	}
	double priceSum = 0;
	for (int i = 0; i < priceList.size(); ++i) {
		priceSum += priceList[i];
	}
	for (int i = 0; i < nameList.size(); ++i) {
		cout << quantList[i] << " of " << nameList[i] << ", $" << priceList[i] << " each" << endl;
	}
	cout << "Your subtotal is: $" << priceSum << endl;
	cout << "Enter your tax percentage:" << endl;
	int tax;
	cin >> tax;
	double tax2 = tax;
	tax2 /= 100;
	tax2 = 1 - tax2;
	double taxedSum;
	taxedSum = tax2 * priceSum;
	cout << "Your total after tax is: $" << taxedSum << endl;
	cout << "Enter your discount percentage:" << endl;
	int discount;
	cin >> discount;
	double disc = discount;
	disc /= 100;
	disc = 1 - disc;
	double discSum;
	discSum = disc * taxedSum;
	cout << "Your total discounted price is: $" << discSum << endl;
	return 0;
}
