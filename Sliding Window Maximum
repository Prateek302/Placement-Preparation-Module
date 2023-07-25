class Solution {

	/*
		Time Complexity : O(N)
		Space Complexity : O(K)
	*/

public:
    vector<int> maxSlidingWindow(vector<int>& nums, int k) {
        deque<int> dq;
        int n = nums.size();
        vector<int> res;
        
        for(int i=0; i<k; i++){
            while(dq.size()>0 && dq.back()<nums[i]){
                dq.pop_back();
            }
            
            dq.push_back(nums[i]);
        }
        
        res.push_back(dq.front());
        
        for(int i=k; i<n; i++){
            int addIdx = i;
            int rmvIdx = i-k;
                        
            // expand the window
            while(dq.size()>0 && dq.back()<nums[addIdx]){
                dq.pop_back();
            }
            
            dq.push_back(nums[addIdx]);
            
            // compress the window
            if(dq.front() == nums[rmvIdx]){
                dq.pop_front();
            }
            
            res.push_back(dq.front());
        }
        
        return res;
    }
};
