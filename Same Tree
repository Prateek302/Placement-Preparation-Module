/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    int level=0;
    queue<TreeNode*>tobetraversed;
    void Traverse(vector<vector<int>>&ans)
    {
        int thisiteration=tobetraversed.size();
        vector<int>values;
        while(thisiteration--)
        {
            if(tobetraversed.front()==NULL)
            {
                tobetraversed.pop();
                continue;
            }
            if(tobetraversed.front()->left!=NULL)
            {
                tobetraversed.push(tobetraversed.front()->left);
            }
            if(tobetraversed.front()->right!=NULL)
            {
                tobetraversed.push(tobetraversed.front()->right);
            }
            values.push_back(tobetraversed.front()->val);
            tobetraversed.pop();
        }
        if(level%2==1)
        {
            reverse(values.begin(),values.end());
        }
        level++;
        ans.push_back(values);
        if(tobetraversed.size()!=0)
        {
            Traverse(ans);
        }
        return;
    }
    vector<vector<int>> zigzagLevelOrder(TreeNode* root) {
        vector<vector<int>>ans;
        if(root==NULL)
        {
            return ans;
        }
        tobetraversed.push(root);
        Traverse(ans);
        return ans;
    }
};
