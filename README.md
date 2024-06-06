Write a program to implement Bresenham’s line drawing algorithm.

#include <stdio.h>

void bresenhamLine(int x0, int y0, int x1, int y1) {
    int dx = abs(x1 - x0), dy = abs(y1 - y0);
    int sx = (x0 < x1) ? 1 : -1;
    int sy = (y0 < y1) ? 1 : -1;
    int err = dx - dy;

    while (1) {
        printf("(%d, %d)\n", x0, y0);
        if (x0 == x1 && y0 == y1) break;
        int e2 = 2 * err;
        if (e2 > -dy) {
            err -= dy;
            x0 += sx;
        }
        if (e2 < dx) {
            err += dx;
            y0 += sy;
        }
    }
}

int main() {
    int x0 = 0, y0 = 0, x1 = 6, y1 = 4;
    bresenhamLine(x0, y0, x1, y1);
    return 0;
}
