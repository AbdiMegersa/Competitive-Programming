class Solution:
    def numIdenticalPairs(self, nums: List[int]) -> int:
        pairs=0
        for i in range(len(nums)):
            j=i+1
            while j<len(nums):
                if nums[i]==nums[j]:
                    pairs+=1
                j+=1
        return pairs
