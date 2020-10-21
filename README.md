# Myleet
# 二分法
class Solution {
public:
    int guessNumber(int n) {
        int a = 1, r = n;
        while(a<=r)
        {
            int mid = a+(r-a)/2;
            if(guess(mid)==0){return mid;}
            else if (guess(mid)==-1){r=mid-1;}
            else {a=mid+1;}
        }
        return -1;
    }
};

# 贪心
class Solution {
public:
    int findContentChildren(vector<int>& g, vector<int>& s) {
        int ng=0;int nc=0;
        std::sort(g.begin(),g.end());
        std::sort(s.begin(),s.end());
        while(ng<g.size()&& nc<s.size())
        {
            if(s[nc]>=g[ng])
            {
                ng++;
            }
            nc++;
        }
        return ng;


    }
};
