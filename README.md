# JavaPractice-Day1
2차 방정식의 근을 구하는 프로그램을 작성하여 보자. 즉 b와 c의 갓\ㅄ이 주어진 상태에서 x*x + b*x + c 식의 근을 계산하는 것이다. 
단 근은 모두 실수라고 가정라자. 예를 들어서 b = -3.0, c = 2.0인 경우에는 2.0과 1.0이 근이된다.

* 실행결과 
* 근은 2.0
* 근은 1.0
~~~
package Lab;

public class QuadraticEquationRoot {
	public static void main(String args[]) {
		double root1, root2;
		double a = 1, b = -3.0, c = 2.0;

		double middleR = b * b - 4 * a * c;

		root1 = (-b + Math.sqrt(middleR)) / 2;
		root2 = (-b - Math.sqrt(middleR)) / 2;

		System.out.println("근은 " + root1);
		System.out.println("근은 " + root2);
	}
}
-------------------------------------------------------------------------------------------------------------------------------
</br>

사용자로부터 원의 반지름을 입력받고 이 원의 면적을 구한 다음, 화면에 출력한다.
입력 단계, 처리 단계, 출력 단계로 구성되어 있다. 원의 면적을 구하여면 실수형 계산을 하여야 한다. */

* 실행결과
* 반지름을 입력하시오: 5
* 78.5
~~~
package Lab;
import java.util.*;

public class CircleArea {
	public static void main(String args[]){		
		Scanner sc = new Scanner(System.in);
		int r;
		double area;
		
		System.out.print("반지름을 입력하시오: ");
		r = sc.nextInt();
		
		area = r*r*3.14;
		System.out.println(area);
	}
}
------------------------------------------------------------------------------------------------------------------------------------
package Lab;
// 사용자로부터 직사각형의 가로와 세로를 받아서 둘레와 면적을 구하는 프로그램을 작성.

/* 실행결과
 * 사각형의 가로를 입력하시오: 10
 * 사각형의 세로를 입력하시오: 5
 * 사각형의 넓이는 50.0
 * 사각형의 둘레는 30.0 */

import java.util.*;

public class Rectangle {
	public static void main(String args[]){		
		int w, h;
		double area;
		double perimeter;
		
		Scanner sc = new Scanner(System.in);
		System.out.print("사각형의 가로를 입력하시오: ");
		w = sc.nextInt();
		System.out.print("사각형의 세로를 입력하시오: ");
		h = sc.nextInt();
		
		area = w*h;
		perimeter = (w+h) *2;
		System.out.println("사각형의 넓이는 " + area);
		System.out.println("사각형의 둘레는 " + perimeter);
	}
}
----------------------------------------------------------------------------------------------------------------------------------
package Lab;
/* 학생들의 성적을 받아 학점을 출력하는 프로그램을 작성하여 실행.
 * 성적 90이상 A, 80이상 90미만 B, 70이상 80미만 C, 60이상 70미만 D, 나머지 F */

/* 실행결과
 * 성적을 입력하시오: 92
 * 학점 A */
import java.util.*;

public class Grade {
	public static void main(String args[]) {
		int score, n;
		char gd;

		Scanner sc = new Scanner(System.in);
		System.out.print("성적을 입력하시오: ");
		score = sc.nextInt();
		n = score / 10;
		
		switch (n) {
		case 10:
		case 9:
			gd = 'A';
			break;
		case 8:
			gd = 'B';
			break;
		case 7:
			gd = 'C';
			break;
		case 6:
			gd = 'D';
			break;
		default:
			gd = 'F';
			break;
		}
		System.out.println("학점: " + gd);
	}
}
------------------------------------------------------------------------------------------------------------------------------------
package Lab;
/* 현재 시각을 받아서 적절한 인사를 출력.
 * 현재 시각에 따라 연속적인 if문 사용. */

/* 실행결과
 * 현재시간은 Thu Aug 06 10:15:27 KST 2015
 * Good Moring
 * 
 * 현재시간은 Thu Aug 06 22:15:27 KST 2015
 * Good Evening */
import java.util.Date;

public class Greeting {
	public static void main(String args[]) {
		Date d = new Date(); //현재 시각을 불러옴
		int currentHour = d.getHours(); //시간

		System.out.println("현재시간은  " + d);

		if (currentHour < 11)
			System.out.println("Good Morning");
		else if (currentHour < 15)
			System.out.println("Good Afternoon");
		else if (currentHour < 20)
			System.out.println("Good Evening");
		else
			System.out.println("Good Night");
	}
}
------------------------------------------------------------------------------------------------------------------------------------
