class Solution {
    bool isvalid=true;
public:
    int height(TreeNode* &root){
        if(!root) return 0;
        int lh=height(root->left);
        int rh=height(root->right);
        if(isvalid&& abs(lh-rh)>1)
            isvalid=false;
        return max(lh,rh)+1;
    }
    bool isBalanced(TreeNode* root) {
        height(root);
        return isvalid;
    }
};
