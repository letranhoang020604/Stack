# Stack
package basic.dev;

import java.util.Scanner;
import java.util.Stack;

public class lehoang {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		Stack<Integer> s = new Stack<Integer>();
		s.push(1);
		s.push(2);
		s.push(3);
		
        int count = s.size();
        System.out.println("so phan tu stack: " + count);
        System.out.println("nhap phan tu muon xuat: ");
        int n = sc.nextInt();
        System.out.println("phan tu trong stack: " + s.get(n-1));
        System.out.println("noi dung cua stack: " + s);
        System.out.println("nhap phan tu muon loai: ");
        int indexToRemove = sc.nextInt();
        int removedElement = s.remove(indexToRemove);
        System.out.println("loai phan tu " + indexToRemove + ": " + removedElement);
        
        System.out.println("phan tu goc: " + s);
        Stack<Integer> tempStack = new Stack<Integer>();
        while (!s.isEmpty()) {
        	tempStack.push(s.pop());
        }
        s = tempStack;
        System.out.println("Phan tu dao: " + s);
	}
}
