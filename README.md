# Check-if-an-array-is-subset-of-another-array
Check if an array is subset of another array.
#include <iostream>
#include <vector>
#include<unordered_map>
using namespace std;
vector<int>removedup(vector<int> &a,int size)
{   vector<int>result;
    unordered_map<int,bool>seen;
    for(int i=0;i<size;i++)
    {
        if(seen.count(a[i])==1)   //if it inserted in map then value changes 0->1;
        continue;                  // if we already have this value , continue.either we add it to map and result.
    
    seen.insert({a[i],1});
    result.push_back(a[i]);
}
return result;
}
int main()
{
    vector<int> a={1,2,2,3,4,5,6,5,4};
    vector<int>result=removedup(a,9);
    for(int i=0;i<result.size();i++)
    {
        cout<<result[i] <<" ";
    }

}
