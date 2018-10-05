# Marquez34
Assignment2
Write a short program, in any programming language, that implements the Caesar substitution cipher with k=3. That is, each letter in the input plaintext should be shifted by 3 positions (e.g., a is replaced by d, b is replaced by e, and so on). The program should prompt for the plain text and then output the corresponding ciphertext.
 
#include <iostream> 
using namespace std; 

#include<iostream>
 
using namespace std;
 
int main()
{
    char message[100], ch;
    int i, key;
    
    cout << "HELLO WORLD: ";
    cin.getline(message, 100);
    cout << "3: ";
    cin >> key;
    
    for(i = 0; message[i] != '\0'; ++i){
        ch = message[i];
        
        if(ch >= 'a' && ch <= 'z'){
            ch = ch + key;
            
            if(ch > 'z'){
                ch = ch - 'z' + 'a' - 1;
            }
            
            message[i] = ch;
        }
        else if(ch >= 'A' && ch <= 'Z'){
            ch = ch + key;
            
            if(ch > 'Z'){
                ch = ch - 'Z' + 'A' - 1;
            }
            
            message[i] = ch;
        }
    }
    
    cout << "KHOOR ZRUOG: " << message;
    
    return 0;
