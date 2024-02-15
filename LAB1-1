#include <iostream>
#include <cmath>
#include <iomanip>

using namespace std;

namespace my_unique_namespace {

    int sizechecker() {
        int n;

        cout << "Enter the size of the array: ";

        while (true) {
            try {
                if (!(cin >> n)) {
                    cin.clear();

                    while (cin.get() != '\n');

                    throw "Size is non-digit!";
                } else if (n <= 0 || n > 10) {
                    throw "Size is out of range!";
                } else {
                    break;
                }
            } catch (const char* exception) {
                cout << exception << '\n';

                cout << "Please enter a new size: ";
            }
        }
        return n;
    }

    int checkelem(int n) {
        int elem;

        cout << "Enter an element: ";

        while (true) {
            try {
                if (!(cin >> elem)) {
                    cin.clear();

                    while (cin.get() != '\n');

                    throw "Element is non-digit!";
                } else {
                    break;
                }
            } catch (const char* exception) {
                cout << exception << '\n';

                cout << "Please enter a new element: ";
            }
        }
        return elem;
    }

    double checkparam(int n) {
        double param;

        cout << "Enter a parameter: ";

        while (true) {
            try {
                if (!(cin >> param)) {
                    cin.clear();

                    while (cin.get() != '\n');

                    throw "Parameter is non-digit!";
                } else {
                    break;
                }
            } catch (const char* exception) {
                cout << exception << '\n';

                cout << "Please enter a new parameter: ";
            }
        }
        return param;
    }

    void finder(double A, double B, int n, int* arr) {
        int k = 0;

        cout << "Indexes of found elements: ";

        for (int i = 0; i < n; i++) {
            if (arr[i] > A && arr[i] < B) {
                k++;

                cout << i << " ";
            }
        }

        cout << endl;

        if (k > 0)
            cout << "Number of elements greater than A and less than B: " << k;
        else
            cout << "Nothing found!";
    }

    int main() {
        int n;

        double A, B;

        n = sizechecker();

        int* arr = new int[n];

        for (int i = 0; i < n; i++)
            arr[i] = checkelem(n);

        here:
        A = checkparam(n);

        B = checkparam(n);

        if (A == B || A > B) {
            cout << "Parameter A should be less than B!\n";

            goto here;
        }

        finder(A, B, n, arr);

        delete[] arr;

        return 0;
    }

} // namespace my_unique_namespace

int main() {
    return my_unique_namespace::main();
}
