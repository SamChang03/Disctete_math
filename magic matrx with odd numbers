#include <iostream>
using namespace std;

/***n is odd***/

int main(){

    /***set the (odd) number of rows and columns***/
    const int n = 7;

    /***set default***/
    int M[n][n]= {0};
    int i, j;
    int r = 0, c = (int) (n / 2);

    /***operation (let the number go top left from small to large)***/
    M[r][c] = 1; // start point

    for (int step = 2; step <= n*n; step++){
        r = (r - 1 + n)  % n;
        c = (c -1 + n) % n;

        if (M[r][c] != 0) {
            r = (r + 2) % n;
            c = (c + 1) % n;
        }
        M[r][c] = step;
    }

    /***show the matrix***/
    for(i = 0; i< n;i++){
        for(j = 0; j< n;j++){
            if (M[i][j] < 10) cout << " ";
            cout << M[i][j] << " " ;
        }
        cout << endl;
    }
    cin >> i;
}
