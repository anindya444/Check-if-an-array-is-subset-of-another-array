# Check-if-an-array-is-subset-of-another-array
# Check if an array is subset of another array.-->> using Hashing.

using namespace std;
#include <iostream>
#include <vector>
#include<unordered_map>
bool isSubset(vector<int>& a, vector<int>& b) {
 unordered_map<int,bool>mp;
   for(int i=0;i<a.size();i++)
   {
     mp[a[i]]=true;
   }
 for(int j=0;j<b.size();j++)
 {
   if( mp.count(b[j])==0)
    {
        return false;
    }
 }
return true;
}

int main() {
    vector<int> a = {1, 19, 13, 21, 3, 7,11};
    vector<int> b = {11, 34, 7, 1};
  
    if (isSubset(a, b)) {
        cout << "true" << endl;
    } else {
        cout << "false" << endl;
    }

    return 0;
}
