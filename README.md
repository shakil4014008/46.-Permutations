# 46.-Permutations
py
````py

class Solution:
    def permute(self, nums: List[int]) -> List[List[int]]:
        
        # if self is not ncessary no use, it use memory
        def backtrack( first  = 0 ) -> List[List[int]]: 
            if first == n: 
                a.append(nums[:]) # as it is a stack, when pop, first value reset to prev one
            
            for i in range(first, n):
                nums[i], nums[first] = nums[first], nums[i]
                # print(i,first,  n, end = " ")
                print(i, end = " ")
                backtrack(first + 1)

                nums[i], nums[first] = nums[first], nums[i]
            
            return a
            
        
        a = []
        n = len(nums)
        backtrack()
        return a 
````
