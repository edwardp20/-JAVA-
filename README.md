# -JAVA-
一个简单的小程序-
`GuessNumber.java`（猜数字游戏）

```java
import java.util.Scanner;
import java.util.Random;

public class GuessNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        
        int number = random.nextInt(100) + 1;
        int guess = 0;
        int tries = 0;
        
        System.out.println("🎯 猜数字游戏 (1-100)");
        
        while (guess != number) {
            System.out.print("请输入你的猜测: ");
            guess = scanner.nextInt();
            tries++;
            
            if (guess < number) {
                System.out.println("猜小了！");
            } else if (guess > number) {
                System.out.println("猜大了！");
            } else {
                System.out.println("🎉 恭喜猜对了！");
                System.out.println("你用了 " + tries + " 次机会");
            }
        }
        
        scanner.close();
    }
}
