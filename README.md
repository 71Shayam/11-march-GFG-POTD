	int countPairs(vector<vector<int>> &mat1, vector<vector<int>> &mat2, int n, int x)
	{
	    // Your code goes here
	    int i=0,j=0,k=n-1,l=n-1,ans=0;
	    while(i<n and j<n and k>=0 and l>=0){
	        if(mat1[i][j]+mat2[k][l]==x){
	            ans++;
	            if(j==n-1){
	                j=0;
	                i++;
	            }
	            else j++;
	            if(l==0){
	                l=n-1;
	                k--;
	            }
	            else l--;
	        }
	        else if(mat1[i][j]+mat2[k][l]>x){
	            if(l==0){
	                l=n-1;
	                k--;
	            }
	            else l--;
	        }
	        else{
	            if(j==n-1){
	                j=0;
	                i++;
	            }
	            else j++;
	        }
	    }
	    return ans;
	}
