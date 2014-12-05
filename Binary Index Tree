//Binary Indexed Tree -> Range update and Range Query
#include <bits/stdc++.h>
#define forall(i,a,b)               for(int i=a;i<=b;i++)
#define pb                          push_back
#define mp 							make_pair
#define INDEX(arr,ind)               (lower_bound(all(arr),ind)-arr.begin())
#define mod                          1000000007

#define TRvi(c, it) \
for (vi::iterator it = (c).begin(); it != (c).end(); it++)
#define TRvii(c, it) \
for (vii::iterator it = (c).begin(); it != (c).end(); it++)
#define TRmsi(c, it) \
for (msi::iterator it = (c).begin(); it != (c).end(); it++)

using namespace std;

typedef long long ll;
typedef vector<int> vi;
typedef pair<int, int> ii;
typedef vector<ii> vii;
typedef set<int> si;
typedef map <string, int> msi;


ll MaxVal=100005;
ll tree1[100005], tree2[100005];


ll read1(ll idx){
	ll sum = 0;
	while (idx > 0){
		sum += tree1[idx];
		idx -= (idx & -idx);
	}
	return sum;
}

void update1(ll idx ,ll val){
	while (idx <= MaxVal){
		tree1[idx] += val;
		idx += (idx & -idx);
	}
}

ll read2(ll idx){
	ll sum = 0;
	while (idx > 0){
		sum += tree2[idx];
		idx -= (idx & -idx);
	}
	return sum;
}

void update2(ll idx ,ll val){
	while (idx <= MaxVal){
		tree2[idx] += val;
		idx += (idx & -idx);
	}
}




int main()
{
	 #ifndef ONLINE_JUDGE
     //freopen("in.txt","r",stdin);
     #endif
	 ios_base::sync_with_stdio(false);

	int t;
	cin>>t;
	
	while(t--)
	{	
	
		//tree1=new int[100001];tree2=new int[100001];
		ll n,c;
		cin>>n>>c;
	//	forall(i,1,n){update1(i,0);update2(i,0);}
	memset(tree1, 0, (n+1) * sizeof(ll));
		memset(tree2, 0, (n+1) * sizeof(ll));
		while(c--)
		{
			ll ch,p,q,v;
			cin>>ch>>p>>q;
			if(ch==0)
			{
				cin>>v;
				update1(p,v);update1(q+1,-v);
				//update2(p,v*(p-1));update2(q+1,-v*q);
			}
			else
			{
				ll ans,temp;
				ans=((read1(q)*q-read2(q)) - (read1(p-1)*(p-1)-read2(p-1)));
				cout<<ans<<endl;
			}
		}



	}
	return 0;
}


