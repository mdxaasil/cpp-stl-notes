# C++ - STL

## **VECTOR**

vector <int> v; // empty vector
vector <int> v(5); // of size 5, but all 0
vector <int> v(5,1); //all ones

v.push_back(x); v.pop_back();
v.begin()   v.end()

## **SORT**

sort(startPointer,endPointer)
sort(arr, arr + n, greater<int>()); //descending order

## **PAIR**

pair<int,string> p = {4,"hey"};
p.first=12;
p.second="bye";

## **ITERATORS**

vector<int> v= {10,15,12,5,20};

auto it=v.begin(); //auto assigns the datatype automatically 

it can now be used for iterating just like a normal pointer

## **SET**

> unique | sorted | no random access (i.e. use iterators/pointers)
> 

set<int> s; //empty set of integers

set<string> s; //empty set of strings

s.insert(x);

s.insert(x);

s.erase(x); 

s.clear()’

Set Iterators

s.begin() //points to the smallest element of the set because set is sorted

s.find(x)

s.erase(it) 

s.end() // is the iterator of non-existant element

Searching for an element in SET

s.find(x)==s.end() //not found

s.count(x)==0 //not found

## -**COUNT**

s.count(x); //for set

count(v.begin(),v.end(),x); //for vector

count(str.begin(),str.end(),'y'); // in  a string

## **MAP**

map<key_dataType, value_dataType>

> sorted according to keys ( similar to set) | keys are unique | useful for counting frequencies
> 

m.clear() //clears a map

m[key] - value for the corresponding key - O(logN)

eg:

map<string, double> m;

//insert some values in map

auto it= m.fin d(”aasil”);

pair<string, double> p  = *it; // { ”aasil”, m[”aasil”] }

**Note**: if you try to search for a value with a key which is not existing, then it creates the element with the searched key and the value assigned is 0.    

## **ITERATING CONTAINERS**

->Conventional method: // **works for map/set/vector**

for (auto it = s.begin() ; it ≠ s.end(); it++)

{

//*it

}

->Shorthand method:

vector <int> v;

for (int x:v){

//x

}

set<int> s;

for(int x:s){

//x

}

map<int ,int> x;

for (pair<int,int> x: v){

//x.first, x.second

}

  
## **upper_bound**

returns an iterator pointing to the first element in the range [first, last)
Problem reference: https://www.codechef.com/viewsolution/73561721
  
**Note**: In map its key value pair because x.first is key, x.second is value.

## **priority_queue**
Specifically designed such that the first element of the queue is either 
the greatest or the smallest of all elements in the queue and elements are in 
**nonincreasing order.**

priority_queue<int> g ;
  
**Extra:**

A shop has objects (key - name , value- price). Get the cheapest

then, set(pair<int,string>)
