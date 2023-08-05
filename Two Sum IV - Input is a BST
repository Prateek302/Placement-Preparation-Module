class Solution {
    void solve(TreeNode* root, vector<int> & inorder){
        if(root==NULL)
            return ;
            // LNR
        solve(root->left,inorder);
        inorder.push_back(root->val);
        solve(root->right,inorder);
    }
public:
    bool findTarget(TreeNode* root, int k) {
        vector<int> inorder;
        solve(root,inorder);
        int s=0,e=inorder.size()-1;
        int sum=0;
        while(s<e)
        {
            sum=inorder[s]+inorder[e];
            if(sum==k)
                return true;
            else if (sum>k)
                e--;
            else
                s++;
        }
        return false;
    }
};
