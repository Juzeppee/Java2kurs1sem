## Задача 1 ##
### Напишите программу, которая конвертирует сумму денег из китайских юаней в российские рубли по курсу покупки 11.91. ###
```java
import java.util.Scanner;
public class main {
    public static void main(String[] args){
        final double ROUBLES_PER_YUAN = 11.91;
        int yuan;
        Scanner input = new Scanner(System.in);
        System.out.print("Введите сумму в юанях: ");
        yuan = input.nextInt();
        if (yuan<=0)
            System.out.println("Введено неверное значение, количество юаней положительное число");
        else {
            double roubles;
            System.out.println("Сумма в рублях состовляет: " + roubles);
        }
    }
}
```


## Задача 2 ##
### Перепишите программу, которая конвертирует сумму денег из китайских юаней в российские рубли по курсу покупки 11.91, добавив структуру выбора для принятия решений об окончаниях входной валюты в зависимости от ее значения. ### 
```java
import java.util.Scanner;
public class ConvectYuan {
    public static void main(String[] args){
        final double ROUBLES_PER_YUAN = 11.91;
        int yuan, digit, digit2;
        Scanner input = new Scanner(System.in);
        System.out.print("Введите сумму денег в юянях: ");
        yuan = input.nextInt();
        if (yuan <= 0)
            System.out.println("Введено неверное значение, значение должно быть полож.");
        else {
            digit = yuan % 10;
            digit2 = (yuan / 10) %10;
            if (digit == 1 && digit2 != 1)
                System.out.println("Был введен " + yuan + " юань.");
            else if (digit > 1 && digit < 5 && digit2 !=1) {
                System.out.println("Было Введено " + yuan + " юаня.");
            } else
                System.out.println("Было введено " + yuan + " юаней.");
            double roubles;
            roubles = ROUBLES_PER_YUAN * yuan;
            System.out.println("Сумма денег в рублях составляет " + roubles);
        }
    }
}
