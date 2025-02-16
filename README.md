#include <stdio.h>
#include <graphics.h>  // You need to link the graphics.h library in your compiler

// Midpoint Circle Drawing Algorithm
void midpointCircle(int xc, int yc, int r) {
    int x = 0, y = r;
    int p = 1 - r; // Decision parameter

    // Draw the initial points
    putpixel(xc + x, yc + y, WHITE);
    putpixel(xc - x, yc + y, WHITE);
    putpixel(xc + x, yc - y, WHITE);
    putpixel(xc - x, yc - y, WHITE);
    putpixel(xc + y, yc + x, WHITE);
    putpixel(xc - y, yc + x, WHITE);
    putpixel(xc + y, yc - x, WHITE);
    putpixel(xc - y, yc - x, WHITE);

    // Loop to draw the other points
    while (x < y) {
        x++;

        if (p < 0) {
            p = p + 2 * x + 1;
        } else {
            y--;
            p = p + 2 * (x - y) + 1;
        }

        // Draw the points
        putpixel(xc + x, yc + y, WHITE);
        putpixel(xc - x, yc + y, WHITE);
        putpixel(xc + x, yc - y, WHITE);
        putpixel(xc - x, yc - y, WHITE);
        putpixel(xc + y, yc + x, WHITE);
        putpixel(xc - y, yc + x, WHITE);
        putpixel(xc + y, yc - x, WHITE);
        putpixel(xc - y, yc - x, WHITE);
    }
}

int main() {
    int xc, yc, r;
    
    // Initialize graphics mode
    int gd = DETECT, gm;
    initgraph(&gd, &gm, "C:\\TurboC3\\BGI");

    // Get user input for circle center and radius
    printf("Enter the center coordinates (xc, yc): ");
    scanf("%d %d", &xc, &yc);
    printf("Enter the radius: ");
    scanf("%d", &r);

    // Draw the circle
    midpointCircle(xc, yc, r);

    // Wait for user input before closing the graphics window
    getch();
    closegraph();

    return 0;
}EX 1 C 
#include <stdio.h>
#include <graphics.h>  // You need to link the graphics.h library in your compiler

// Midpoint Circle Drawing Algorithm
void midpointCircle(int xc, int yc, int r) {
    int x = 0, y = r;
    int p = 1 - r; // Decision parameter

    // Draw the initial points
    putpixel(xc + x, yc + y, WHITE);
    putpixel(xc - x, yc + y, WHITE);
    putpixel(xc + x, yc - y, WHITE);
    putpixel(xc - x, yc - y, WHITE);
    putpixel(xc + y, yc + x, WHITE);
    putpixel(xc - y, yc + x, WHITE);
    putpixel(xc + y, yc - x, WHITE);
    putpixel(xc - y, yc - x, WHITE);

    // Loop to draw the other points
    while (x < y) {
        x++;

        if (p < 0) {
            p = p + 2 * x + 1;
        } else {
            y--;
            p = p + 2 * (x - y) + 1;
        }

        // Draw the points
        putpixel(xc + x, yc + y, WHITE);
        putpixel(xc - x, yc + y, WHITE);
        putpixel(xc + x, yc - y, WHITE);
        putpixel(xc - x, yc - y, WHITE);
        putpixel(xc + y, yc + x, WHITE);
        putpixel(xc - y, yc + x, WHITE);
        putpixel(xc + y, yc - x, WHITE);
        putpixel(xc - y, yc - x, WHITE);
    }
}

int main() {
    int xc, yc, r;
    
    // Initialize graphics mode
    int gd = DETECT, gm;
    initgraph(&gd, &gm, "C:\\TurboC3\\BGI");

    // Get user input for circle center and radius
    printf("Enter the center coordinates (xc, yc): ");
    scanf("%d %d", &xc, &yc);
    printf("Enter the radius: ");
    scanf("%d", &r);

    // Draw the circle
    midpointCircle(xc, yc, r);

    // Wait for user input before closing the graphics window
    getch();
    closegraph();

    return 0;
}
