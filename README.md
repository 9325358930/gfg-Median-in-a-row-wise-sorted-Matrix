***Median in a row-wise sorted Matrix***  

Given a row wise sorted matrix of size R*C where R and C are always odd, find the median of the matrix

Example 1:

Input:
R = 3, C = 3
M = [[1, 3, 5], 
     [2, 6, 9], 
     [3, 6, 9]]
Output: 5
Explanation: Sorting matrix elements gives 
us {1,2,3,3,5,6,6,9,9}. Hence, 5 is median. 

class Solution{   
public:
    int median(vector<vector<int>> &matrix, int R, int C){
        // code here   
        vector<int> vec;
        int size = R*C;
        for(int i = 0; i<R; i++){
            for(int j = 0; j<C; j++){
                vec.push_back(matrix[i][j]);
            }
        }
        sort(vec.begin(), vec.end());
        int mid = ((size+1)/2);
        int a = vec[mid -1];
        return a;
    }
};
