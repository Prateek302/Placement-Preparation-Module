class Solution {
public:
    vector<int> topKFrequent(vector<int>& nums, int k) {
        vector<int> ans;
        int n=nums.size();
        unordered_map<int,int> mp;
        for(int i=0;i<n;i++){
            mp[nums[i]]++;
        }
        set<int> st(nums.begin(),nums.end());
        priority_queue<pair<int,int>>  pq;
        set<int>::iterator itr;
        for (itr = st.begin();itr != st.end(); itr++){
             pq.push({mp[*itr],*itr});
        }
        while(k--){
            ans.push_back(pq.top().second);
            pq.pop();
        }
        return ans;
    }
};
