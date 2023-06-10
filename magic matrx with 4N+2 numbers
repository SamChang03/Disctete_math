#define N 6


void magic_o(int [][N], int);
void exchange(int [][N], int);

/***n is 4n+2***/

int main() {
    int square[N][N] = {0};

    magic_o(square, N/2);
    exchange(square, N);

    int i, j;
    for(i = 0; i < N; i++) {
        for(j = 0; j < N; j++)
            printf("%2d ", square[i][j]);
        printf("\n");
    }

    return 0;
}

void magic_o(int square[][N], int n) {
    int row = 0;
    int column = n / 2;
    int cnt;
    for(cnt = 1; cnt <= n*n; cnt++) {
        square[row][column] = cnt;
        square[row+n][column+n] = cnt + n*n;
        square[row][column+n] = cnt + 2*n*n;
        square[row+n][column] = cnt + 3*n*n;
        if(cnt % n == 0)
            row++;
        else {
            row = (row == 0) ? n - 1 : row - 1 ;
            column = (column == n-1) ? 0 : column + 1;
        }
    }
}

void exchange(int x[][N], int n) {
    int m = n / 4;
    int m1 = m - 1;

    int i, j;
    for(i = 0; i < n/2; i++) {
        if(i != m)  {
            for(j = 0; j < m; j++)
                swap(x[i][j], x[n/2+i][j]);
            for(j = 0; j < m1; j++)
                swap(x[i][n-1-j], x[n/2+i][n-1-j]);
        }
        else {
            for(j = 1; j <= m; j++)
                swap(x[m][j], x[n/2+m][j]);
            for(j = 0; j < m1; j++)
                swap(x[m][n-1-j], x[n/2+m][n-1-j]);
        }
    }
}
