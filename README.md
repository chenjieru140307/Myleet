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
