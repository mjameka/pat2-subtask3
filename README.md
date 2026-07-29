#include <iostream>
using namespace std;

int main() {
    const int NUM_EXPERIMENTS = 4;
    const int NUM_READINGS = 3;

    cout << "Sparky Electronics - Resistance Testing" << endl;
    cout << "=======================================" << endl;

    for (int experiment = 1; experiment <= NUM_EXPERIMENTS; experiment++) {
        double reading;
        double total = 0.0;
        double average;

        cout << "\nExperiment " << experiment << endl;
        cout << "Enter " << NUM_READINGS << " readings:" << endl;

        for (int i = 1; i <= NUM_READINGS; i++) {
            cout << "Reading " << i << ": ";
            cin >> reading;
            total = total + reading;
        }

        average = total / NUM_READINGS;

        cout << "Average resistance: " << average << " ohms - ";
        
        if (average < 100) {
            cout << "Below acceptable range" << endl;
        }
        else if (average >= 100 && average <= 300) {
            cout << "Within acceptable range" << endl;
        }
        else {
            cout << "Above acceptable range" << endl;
        }
    }

    cout << "\nTesting complete. All " << NUM_EXPERIMENTS << " experiments done." << endl;
    return 0;
}
