#include <iostream>
#include <cmath>
#include <vector>
#include <algorithm>
#include <numeric>
#include <map>
#include <set>
#include <typeinfo>

using namespace std;

int main() {
    // 1. cout (Equivalent to Python print())
    cout << "Hello, World!" << endl;

    // 2. Type Checking (C++ uses typeid)
    cout << "Type of 10: " << typeid(10).name() << endl;
    cout << "Type of 3.14: " << typeid(3.14).name() << endl;
    cout << "Type of 'C++': " << typeid("C++").name() << endl;

    // 3. Length (for strings & vectors)
    string str = "C++";
    cout << "Length of string: " << str.length() << endl;
    vector<int> vec = {1, 2, 3, 4, 5};
    cout << "Size of vector: " << vec.size() << endl;

    // 4. Absolute Value
    cout << "Absolute of -10: " << abs(-10) << endl;

    // 5. Rounding (floor, ceil, round)
    cout << "Round(3.456): " << round(3.456) << endl;
    cout << "Floor(3.456): " << floor(3.456) << endl;
    cout << "Ceil(3.456): " << ceil(3.456) << endl;

    // 6. Max and Min
    cout << "Max(10, 20): " << max(10, 20) << endl;
    cout << "Min(10, 20): " << min(10, 20) << endl;

    // 7. Sum of vector elements
    cout << "Sum of vector elements: " << accumulate(vec.begin(), vec.end(), 0) << endl;

    // 8. Sorting
    vector<int> numbers = {3, 1, 4, 1, 5, 9};
    sort(numbers.begin(), numbers.end());
    cout << "Sorted numbers: ";
    for (int num : numbers) cout << num << " ";
    cout << endl;

    // 9. User Input
    // Uncomment for user input testing
    // string name;
    // cout << "Enter your name: ";
    // cin >> name;
    // cout << "Hello, " << name << endl;

    // 10. Type Conversion
    int num1 = stoi("10");
    double num2 = stod("3.14");
    string strNum = to_string(100);
    cout << "stoi('10'): " << num1 << endl;
    cout << "stod('3.14'): " << num2 << endl;
    cout << "to_string(100): " << strNum << endl;

    // 11. Vector, Set, Map
    vector<char> charList = {'h', 'e', 'l', 'l', 'o'};
    set<int> numSet = {1, 2, 2, 3}; // Removes duplicates
    map<string, int> person = {{"Alice", 25}, {"Bob", 30}};

    cout << "Vector elements: ";
    for (char c : charList) cout << c << " ";
    cout << endl;

    cout << "Set elements: ";
    for (int n : numSet) cout << n << " ";
    cout << endl;

    cout << "Map values: Alice=" << person["Alice"] << ", Bob=" << person["Bob"] << endl;

    // 12. Range Equivalent (for loop)
    cout << "Range(0-4): ";
    for (int i = 0; i < 5; i++) cout << i << " ";
    cout << endl;

    // 13. Enumerate Equivalent (Using index with vector)
    vector<string> fruits = {"apple", "banana", "cherry"};
    cout << "Enumerate equivalent:" << endl;
    for (size_t i = 0; i < fruits.size(); i++) {
        cout << i << " " << fruits[i] << endl;
    }

    // 14. Zip Equivalent (Pairing vectors)
    vector<string> names = {"Alice", "Bob"};
    vector<int> scores = {90, 80};
    cout << "Zip equivalent:" << endl;
    for (size_t i = 0; i < names.size(); i++) {
        cout << names[i] << " " << scores[i] << endl;
    }

    // 15. Map Equivalent (Using transform)
    transform(numbers.begin(), numbers.end(), numbers.begin(), [](int x) { return x * 2; });
    cout << "Map equivalent (x2): ";
    for (int num : numbers) cout << num << " ";
    cout << endl;

    // 16. Filter Equivalent (Using remove_if)
    vector<int> evenNumbers;
    copy_if(numbers.begin(), numbers.end(), back_inserter(evenNumbers), [](int x) { return x % 2 == 0; });
    cout << "Filter equivalent (evens only): ";
    for (int num : evenNumbers) cout << num << " ";
    cout << endl;

    // 17. Eval Equivalent (Simple Calculation)
    cout << "Eval equivalent (10 + 5): " << (10 + 5) << endl;

    // 18. Any() and All() Equivalent
    cout << "Any equivalent (at least one nonzero in {0, 1, 0}): "
         << any_of(vec.begin(), vec.end(), [](int x) { return x > 3; }) << endl;
    cout << "All equivalent (all > 0 in {1, 2, 3}): "
         << all_of(vec.begin(), vec.end(), [](int x) { return x > 0; }) << endl;

    // 19. Memory Address (id Equivalent)
    int x = 10;
    cout << "Memory address of x: " << &x << endl;

    return 0;
}
