# Caesercipher_Encryption
package Caeserprogram;
//Name:              ABIODUN TAOFEEK TIAMIYU
//Student's Number:         21910091
//Course Code:                IT526
//Course Title:     Operating System And Network Security
	import java.util.*;
	
public class Caesercipher_Encryption {
	public static void main(String args[]) {
        Scanner Sc = new Scanner(System.in);
        System.out.println("SOLUTION PROGRAM : ");
        System.out.println("ABIODUN TAOFEEK TIAMIYU : ");
        System.out.println("STUDENT NUMBER: 21910091 : ");
        System.out.println("OPERATING SYSTEM AND NETWORK SECURITY : ");
        System.out.println("ASSIGNMENT 2 : ");
        System.out.println(" Input the plaintext message : ");
        String plaintext = Sc.nextLine();
        System.out.println(" Enter the value by which each character in the plaintext message gets shifted:");
        int shift = Sc.nextInt();
        String ciphertext = "";
        char alphabet;
        for(int i=0; i < plaintext.length();i++) 
        {
             // Shift one character at a time
            alphabet = plaintext.charAt(i);
            
            // if alphabet lies between a and z 
            if(alphabet >= 'a' && alphabet <= 'z') 
            {
             // shift alphabet
             alphabet = (char) (alphabet + shift);
             // if shift alphabet greater than 'z'
             if(alphabet > 'z') {
                // re-shift to starting position 
                alphabet = (char) (alphabet+'a'-'z'-1);
             }
             ciphertext = ciphertext + alphabet;
            }
            
            // if alphabet lies between 'A'and 'Z'
            else if(alphabet >= 'A' && alphabet <= 'Z') {
             // shift alphabet
             alphabet = (char) (alphabet + shift);    
                
             // if shift alphabet greater than 'Z'
             if(alphabet > 'Z') {
                 //re-shift to starting position 
                 alphabet = (char) (alphabet+'A'-'Z'-1);
             }
             ciphertext = ciphertext + alphabet;
            }
            else {
             ciphertext = ciphertext + alphabet;   
            }
        
    }
    System.out.println(" ciphertext : " + ciphertext);
  }
}
