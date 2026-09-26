# Add Two Binary Numbers
# Given two strings a and b, where each string represents a binary number, return the sum of the two binary numbers in decimal form.
# You must convert each binary string into its decimal value and then return their sum.

class Solution {
public:
    string addBinary(string a, string b) {
        int sumx = 0;
        int sumy = 0;
        for (int i = 0; i < a.size(); i++) {     
            if (a[i] == '1') {
                int x = pow(2, a.size() - 1 - i);
                sumx += x;
            }
        }
        for (int i = 0; i < b.size(); i++) {
            if (b[i] == '1') {        
                int y = pow(2, b.size() - 1 - i);
                sumy += y;
            }
        }
        return sumx + sumy;
    }
};
