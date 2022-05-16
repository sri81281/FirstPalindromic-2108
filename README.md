# FirstPalindromic-2108
Example 1:  Input: words = ["abc","car","ada","racecar","cool"] Output: "ada" 
Explanation: The first string that is palindromic is "ada". Note that "racecar" is also palindromic, but it is not the first. 

Example 2:  Input: words = ["notapalindrome","racecar"] Output: "racecar"
Explanation: The first and only string that is palindromic is "racecar".

Example 3:  Input: words = ["def","ghi"] Output: ""
Explanation: There are no palindromic strings, so the empty string is returned.

package LeecodeProblem;

import java.security.DomainCombiner;

public class FirstPalindromic2108 {
 public static String firstPalindrome(String[] words)
 {
	 int check=0;
	 String result="";
	 for(int i=0;i<words.length;i++)
	 {
		  String c=words[i];
		  String com="";
		  for(int j=c.length()-1;j>=0;j--)
		  {
			 com+=c.charAt(j); 
		  }
		  for(int k=0;k<c.length();k++)
		  {
			  check=0;
			  if(c.charAt(k)==com.charAt(k))
			  {
				 check=1; 
			  }
			  else
			  {
				  check=0;
				  break;
			  }
		  }
		  if(check==1)
		  {
			  result=c;
			  break;
		  }
		  
	 }
	 return result;
	 
	 
	
 }
 public static void main(String[] args) {
	String s[]= {"def","ghi"};
	
	String p=firstPalindrome(s);
	System.out.println(p);
}
}


