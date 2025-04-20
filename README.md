#include <stdio.h>

// 加法函数
double add(double a, double b) {
    return a + b;
}

// 减法函数
double subtract(double a, double b) {
    return a - b;
}

// 乘法函数
double multiply(double a, double b) {
    return a * b;
}

// 除法函数
double divide(double a, double b) {
    if (b == 0) {
        printf("错误：除数不能为零。\n");
        return 0;
    }
    return a / b;
}

int main() {
    double num1, num2, result;
    char operator;

    // 提示用户输入数字和运算符
    printf("请输入两个数字和一个运算符（格式：数字 运算符 数字，例如：3 + 5）：");
    scanf("%lf %c %lf", &num1, &operator, &num2);

    switch (operator) {
        case '+':
            result = add(num1, num2);
            printf("%.2lf %c %.2lf = %.2lf\n", num1, operator, num2, result);
            break;
        case '-':
            result = subtract(num1, num2);
            printf("%.2lf %c %.2lf = %.2lf\n", num1, operator, num2, result);
            break;
        case '*':
            result = multiply(num1, num2);
            printf("%.2lf %c %.2lf = %.2lf\n", num1, operator, num2, result);
            break;
        case '/':
            result = divide(num1, num2);
            if (num2 != 0) {
                printf("%.2lf %c %.2lf = %.2lf\n", num1, operator, num2, result);
            }
            break;
        default:
            printf("错误：不支持的运算符。\n");
    }

    return 0;
}    
