const long long N=1e5+7;
vector<bool>pre(N,0);
vector<ll>hp(N,0);
vector<ll>v;
ll f=0;

void precomp()
{
    pre[0]=pre[1]=false;

    for(ll i=2; i<N; i++)
    {
        if(pre[i]==false)
        {
            v.pb(i);
            f++;
            hp[i]=i;
            for(ll j=2*i; j<N; j+=i)
            {
                pre[j]=true;
                hp[j]=i;
            }
        }
    }

}
