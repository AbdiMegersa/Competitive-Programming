class Solution:
    def maxSumTwoNoOverlap(self, nums: List[int], firstLen: int, secondLen: int) -> int:
        F = firstLen
        S = secondLen
        if F + S > len(nums):
            return 0
        for i in range(1, len(nums)):
            nums[i] += nums[i - 1]
            print(nums[i])

        res, max_fir, max_sec = nums[F + S - 1], nums[F - 1], nums[S - 1]
        for i in range(F + S, len(nums)):
            max_fir = max(max_fir, nums[i - S] - nums[i - S - F])
            max_sec = max(max_sec, nums[i - F]- nums[i - F - S])
            res = max(res, max_fir + nums[i]- nums[i - S], max_sec + nums[i] - nums[i - F])

        return res
