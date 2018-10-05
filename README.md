# Marquez34
Assignment2
Write a short program, in any programming language, that implements the Caesar substitution cipher with k=3. That is, each letter in the input plaintext should be shifted by 3 positions (e.g., a is replaced by d, b is replaced by e, and so on). The program should prompt for the plain text and then output the corresponding ciphertext.
 
 #include <iostream> 
  using namespace std;

 
// This function receives text and shift and 
// returns the encrypted text 
  string encrypt (string text, int s) 
{
  
string result = "";
  
 
    // traverse text 
    for (int i = 0; i < text.length (); i++)
    
    {
      
	// apply transformation to each character 
	// Encrypt Uppercase letters 
	if (isupper (text[i]))
	
result += char (int (text[i] + s - 65) % 26 + 65);
      
 
	// Encrypt Lowercase letters 
	else
      
result += char (int (text[i] + s - 97) % 26 + 97);
    
} 
 
    // Return the resulting string 
    return result;

}


 
// Driver program to test the above function 
  int
main () 
{
  
string text = "HELLOWORLD";
  
int s = 3;
  
cout << "Text : " << text;
  
cout << "\nShift: " << s;
  
cout << "\nCipher: " << encrypt (text, s);
  
return 0;

}
