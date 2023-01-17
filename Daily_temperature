class Solution:
    def dailyTemperatures(self, temperatures: List[int]) -> List[int]:
        ans = [0]*len(temperatures)
        stack = []
        for ind, temp in enumerate(temperatures):
            while stack and temp > stack[-1][0]:
                stacktem, stackind = stack.pop()
                ans[stackind] = (ind - stackind)
                
            stack.append([temp, ind])
        return ans
