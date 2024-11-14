# tiktaktoe
game cờ đơn giản
#include <bits/stdc++.h>
using namespace std;
bool check(char dodo[3][3], char player) {
   
    for (int i = 0; i < 3; i++) {
    if (dodo[i][0] == player && dodo[i][1] == player && dodo[i][2] == player)
            return true;
        if (dodo[0][i] == player && dodo[1][i] == player && dodo[2][i] == player)
            return true;
    }
   
    if (dodo[0][0] == player && dodo[1][1] == player && dodo[2][2] == player)
        return true;
    if (dodo[0][2] == player && dodo[1][1] == player && dodo[2][0] == player)
        return true;
    return false;
}
int main (){
	char dodo[3][3];
	for (int i=0;i<3;i++){
		for (int j=0;j<3;j++)
		dodo[i][j]='N';
	}
	cout<<"welcome to x-o designed by NGthanhdo"<<endl;
	for (int i=0;i<3;i++){
		for (int j=0;j<3;j++)
		{
			cout<<dodo[i][j]<<"|";
		}
		cout<<endl;
	}
	int k=9;
	while (k--&& check(dodo,'x')==false && check(dodo,'o')==false){
		if (k%2==0)
	{
			cout <<"moi nguoi choi 1 di ";
			int x,y;
			cin>>x>>y;
			if (dodo[x][y]=='x'||dodo[x][y]=='o')
			cout <<"nuoc di k hop le thang thanh ngu mat luot";
			else{
			
			dodo[x][y]='x';
			for (int i=0;i<3;i++){
		for (int j=0;j<3;j++)
		{
			cout<<dodo[i][j]<<"|";
		}
		cout<<endl;
			}}}
			else{
				cout <<"moi nguoi choi 2 di ";
				int x,y;
			cin>>x>>y;
			if (dodo[x][y]=='x'||dodo[x][y]=='o')
			cout <<"nuoc di k hop le thang thanh ngu mat luot";
			else{
			dodo[x][y]='o';
			for (int i=0;i<3;i++){
		for (int j=0;j<3;j++)
		{
			cout<<dodo[i][j]<<"|";
		}
		cout<<endl;
			}
	}}
	
}
if (check (dodo,'x')==true)
cout <<"player 1 win";
else if (check (dodo,'o')==true)
cout<<"player 2 win";
else
cout <<"hoa roi huhu";
}
