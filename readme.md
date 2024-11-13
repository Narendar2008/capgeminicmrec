```java
import java.util.*;
public class MoveHash{
    public static int moveHash(String str,int n){
        if(str==null){
            return 0;
        }
        String str1="";
        String str2="";
        for(int i=0;i<n;i++){
            if(str.charAt(i)=='#') 
                str1+=str.charAt(i);
            else 
                str2+=str.charAt(i);
        }
        String result=str1.concat(str2);
        System.out.println(result);
        return 1;
    }
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        String a=sc.nextLine();
        int len=(a!=null)?a.length():0;
        int status=moveHash(a,len);
        if(status==0){
            System.out.println(0);
        }
    }
}
```

```c++
#include <iostream>
#include <string>
using namespace std;

void moveHash(const string& str)
{
    // Check if the string is empty
    if (str.empty()) {
        cout << "" << endl;
        return;
    }

    string str1 = "";
    string str2 = "";

    for (char ch : str) {
        if (ch == '#')
            str1 += ch;   // Append '#' characters to str1
        else
            str2 += ch;   // Append other characters to str2
    }

    string result = str1 + str2;
    cout << result << endl;
}

int main()
{
    string a;
    cout << "Enter a string: ";
    getline(cin, a);

    moveHash(a);

    return 0;
}

```
