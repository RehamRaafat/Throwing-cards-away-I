#include <bits/stdc++.h>

using namespace std;

int main()
{
    int n,x;
    while(cin>>n,n){
        queue<int>q;
        vector<int>v;

    for(int i=1; i<=n; i++)
    {
        q.push(i);
    }

    for(int k=0; k<n; k++)
    {
            v.push_back(q.front());
            q.pop();
            q.push(q.front());
            q.pop();
    }
    x=v[n-1];
    if(v.size()==1)
    {
        cout<<"Discarded cards:"<<endl;
        cout<<"Remaining card: "<<x<<endl;
    }
    else{
        cout<<"Discarded cards: ";
        for(int j=0; j<n; j++)
    {
        if(j!=n-1)
        {
            cout<<v[j];
            if(j!=n-2)
            {
                cout<<", ";
            }
        }
        else
        {
            cout<<endl;
            cout<<"Remaining card: "<<x;
        }
    }
    cout<<endl;

    }
    }

    return 0;
}
