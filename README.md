<pre>
#include <iostream>
#include <cmath>
using namespace std;

// f(x)=2x^3−3x^2−12x+5 fonksiyonunun [−2,3] aralığında,
// alabileceği en büyük değer (mutlak maksimum) kaçtır?

double function_q5(double x)
{
    double term1 = 2.0 * pow(x, 3.0);
    double term2 = 3.0 * pow(x, 2.0);
    double term3 = 12.0 * x;
    return term1 - term2 - term3 + 5.0;
}

int main()
{
    cout << "Soru 5: mutlak maksimum değer hesaplama" << endl;

    // Kritik noktalar ve verilen aralık uçları
    double x_values[] = {-2.0, -1.0, 2.0, 3.0};
    double max_value = function_q5(x_values[0]);

    cout << "Kontrol Edilen Noktalar: -2, -1, 2, 3" << endl;

    for (int i = 0; i < 4; ++i)
    {
        double f_x = function_q5(x_values[i]);
        cout << "f(" << x_values[i] << ") = " << f_x << endl;
        if (f_x > max_value)
        {
            max_value = f_x;
        }
    }

    cout << "---------------------------------------------------------" << endl;
    cout << "En büyük değer: " << max_value << endl;

    return 0;

</pre>
