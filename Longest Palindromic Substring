class Solution {
public:
    string longestPalindrome(string s) {
        int start = 0, max_len = 1, tmp_len = 1, same=1;

        for(int i = 1 ; i < s.size() ; i++)
        {
            if(tmp_len == same && s[i-1] == s[i])
            {
                same++;
                tmp_len++;
                if(max_len < tmp_len)
                {
                    max_len = tmp_len;
                    start = i - max_len + 1;
                }
            }
            else if((i-tmp_len-1) >= 0 && s[i-tmp_len-1] == s[i])
            {                
                tmp_len += 2;
                if(max_len < tmp_len)
                {
                    max_len = tmp_len;
                    start = i - max_len + 1;
                }
            }
            else
            {
                i -= tmp_len / 2;
                tmp_len = 1;
                same = 1;
            }
        }

        return s.substr(start, max_len);
    }
};
