# HammeringDistance
The hammering distance between two integers is the number of positions at which the corresponding bits are different

class Solution {
public:
    int hammingDistance(int x, int y) {
        int dist = 0, n = x ^ y;
        while(n){
            ++dist;
            n&=n-1;
        }
        return dist;
    }
};
