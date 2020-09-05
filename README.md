# 58A---Chat-room
#include <bits/stdc++.h>
using namespace std;


int main(){

    queue<char> givenword;
    queue<char> correctword;
    string s="hello";
    for(int i=0;i<s.size();i++){
        correctword.push(s[i]);
    }
    string S;
    cin>>S;
    for(int i=0;i<S.size();i++){
        givenword.push(S[i]);
    }
    while(!correctword.empty() && !givenword.empty()){
        if(givenword.front()==correctword.front()){
            correctword.pop();
            givenword.pop();
        }else{
            givenword.pop();
        }
    }
    if(correctword.empty()){
        cout<<"YES";
    }else cout<<"NO";
}
