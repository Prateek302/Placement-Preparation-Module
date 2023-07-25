class Solution {
public:
    int orangesRotting(vector<vector<int>>& grid) {
        int n=grid.size(),m=grid[0].size();
        int vis[n][m];
        int cntfresh=0;
        int cnt=0;
        queue<pair<pair<int,int>,int>> q;
        for(int i=0;i<n;i++){
            for(int j=0;j<m;j++){
                if(grid[i][j]==2){
                    vis[i][j]=2;
                    q.push({{i,j},0});
                }else{
                    vis[i][j]=0;
                }
                if(grid[i][j]==1) cntfresh++;
            }
        }
        int delr[]={-1,0,1,0};
        int delc[]={0,1,0,-1};
        int tm=0;
        while(!q.empty()){
            int r=q.front().first.first;
            int c=q.front().first.second;
            int t=q.front().second;
            tm=max(tm,t);
            q.pop();
            for(int i=0;i<4;i++){
                int nr=r+delr[i];
                int nc=c+delc[i];
                if(nr>=0 && nc>=0 && nr<n & nc<m && grid[nr][nc]==1 && vis[nr][nc]!=2){
                    q.push({{nr,nc},t+1});
                    vis[nr][nc]=2;
                    cnt++;
                }
            }
        }
        if(cnt!=cntfresh) return -1;
        return tm;
    }
};
