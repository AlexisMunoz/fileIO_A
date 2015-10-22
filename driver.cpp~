// Alexis Muñoz
// 21 October 2015
// 
#include <iostream>
#include <fstream>
#include <cstdlib>
#include <cstring>
using namespace std;

int main(){
    string word, newString, otherString, othercharacter, otherOtherString;
    string character;
    int lengthString = 0;
    int average = 0, count = 0, stringLength = 0 , word1 = 0, word2 = 0, word3 = 0, word4 = 0, word5 = 0, word6 = 0, word7 = 0, word8 = 0, word9 = 0, word10 = 0, word11 = 0;
    
    ifstream fin;
    fin.open("gba.txt");
       
    while (fin >> word){
        
        stringLength += word.length();
        count++;
        
        if ( word.length() == 1){
            word1++;
        }
        else if (word.length() == 2){
            word2++;
        }
        else if (word.length() == 3){
            word3++;
        }
        else if (word.length() == 4){
            word4++;
        }
        else if (word.length() == 5){
            word5++;
        }
        else if (word.length() == 6){
            word6++;
        }
        else if (word.length() == 7){
            word7++;
        }
        else if (word.length() == 8){
            word8++;
        }
        else if (word.length() == 9){
            word9++;
        }
        else if (word.length() == 10){
            word10++;
        }
        else if (word.length() >= 11){
            word11++;
        }
        
        for (lengthString = 0; lengthString < word.length(); lengthString++){
            character = toupper(word[lengthString]);
            newString += character;
            
        }
        newString = newString  + " ";
        
        for (lengthString = 0; lengthString < word.length(); lengthString++){
            othercharacter = toupper(word[0]);
            lengthString++;
            otherString = othercharacter + word.substr(1, word.length() - 1);
        }
         
        //otherOtherString = otherString + " ";
        
        //cout << otherString << endl;
        //cout << " ";
        otherOtherString += otherString + " ";
        
        
    } 
    
    
    average = stringLength / count;
    ofstream fout;
    fout.open("result.txt");  
    fout << "average characters per word: " << average << endl; 
    
    fout << endl << word1 << " words of length 1" << endl;
    fout << word2 << " words of length 2" << endl;
    fout << word3 << " words of length 3" << endl;
    fout << word4 << " words of length 4" << endl;
    fout << word5 << " words of length 5" << endl;
    fout << word6 << " words of length 6" << endl;
    fout << word7 << " words of length 7" << endl;
    fout << word8 << " words of length 8" << endl;
    fout << word9 << " words of length 9" << endl;
    fout << word10 << " words of length 10" << endl;
    fout << word11 << " words of length 11 or longer" << endl;
        
    fout << endl << "total number of words is " << count << endl;
    
    ofstream fout2;
    fout2.open("capitalize.txt");
    fout2 << newString << endl << endl;
     
    ofstream fout3;
    fout3.open("uppercase.txt");
    fout3 << otherOtherString << endl;
    
    fout3.close();
    fout2.close();
    fin.close();
    fout.close();
    return 0;
}
