// hex-to-decimal
#include <iostream>
#include <string.h>
using namespace std;
int main(){
    char hex[20];
    int dec=0,c=1,len;
    cout<<"enter the hexadecimal number: ";
    cin>>hex;
    len = strlen(hex);
    for(int i=len-1;i>=0;i--){
        if(hex[i]>='0' && hex[i]<='9'){
             hex[i]=hex[i]-48;
            dec = dec + c*hex[i];
        }
        else if(hex[i]>='a' && hex[i]<='f'){
            hex[i]=hex[i]-87;
            dec = dec + c*hex[i];
        }
        else if(hex[i]>='A' && hex[i]<='F'){
            hex[i]=hex[i]-55;
            dec = dec + c*hex[i];
        }
        c*=16;
    }
    cout<<dec;
    return 0;
}
