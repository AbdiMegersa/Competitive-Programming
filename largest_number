from typing import List


class Solution:
    def compare(self, num1: int, num2: int):
        return str(num1) + str(num2) > str(num2) + str(num1)

    def sort(self, nums: List[int]) -> List[int]:
        if len(nums) == 1:
            return nums

        mid = len(nums) // 2

        left = self.sort(nums[:mid])
        right = self.sort(nums[mid:])
        return self.merge(left, right)

    def merge(self, arr1: List[int], arr2: List[int]):
        left = 0
        right = 0
        new_arr = []
        while left < len(arr1) or right < len(arr2):
            if left >= len(arr1):
                new_arr.append(arr2[right])
                right += 1
            elif right >= len(arr2):
                new_arr.append(arr1[left])
                left += 1
            elif self.compare(arr1[left], arr2[right]):
                new_arr.append(arr1[left])
                left += 1
            else:
                new_arr.append(arr2[right])
                right += 1
        return new_arr

    def largestNumber(self, nums: List[int]) -> str:
        new_nums = self.sort(nums)
        i = 0
        while i < len(nums) and new_nums[i] == 0:
            i += 1

        if i != 0:
            new_nums = new_nums[i - 1 :]

        return "".join(map(str, new_nums))


if __name__ == "__main__":
    sol = Solution()
    x = sol.compare(38, 3)
    print(x)
