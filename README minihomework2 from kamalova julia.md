#include <iostream>
#include <string>

using namespace std;

string decToOct(int dec) {
  string oct = "";
  if (dec == 0) {
    return "0"; 
  }
  while (dec > 0) {
    int remainder = dec % 8; 
    oct = to_string(remainder) + oct; 
    dec /= 8; 
  }
  return oct;
}

string decToHex(int dec) {
  string hex = "";
  if (dec == 0) {
    return "0"; 
  }
  while (dec > 0) {
    int remainder = dec % 16; 
    if (remainder < 10) { 
      hex = to_string(remainder) + hex;
    } else {  
      char hexDigit = 'A' + (remainder - 10); 
      hex = hexDigit + hex; 
    }
    dec /= 16; 
  }
  return hex;
}

int main() {
  int decNum;
  cout << "Десятичное число: ";
  cin >> decNum;

  cout << "Восьмеричное число: " << decToOct(decNum) << endl;
  cout << "Шестнадцатеричное число: " << decToHex(decNum) << endl;

  return 0;
}







//задание 2

#include<iostream>
using namespace std;

int main(){
    int x;
    cout << "Введите любое натуральное число: ";
    cin >> x;
    
    while (x != 1) { 
        if (x % 2 == 0) {
            x /= 2; 
            cout << x << " "; 
        } else {
            x = (x * 3) + 1; 
            cout << x << " "; 
        }
    }
    cout << endl;
    cout << "Гипотеза верна";
    return 0;
} 


   
