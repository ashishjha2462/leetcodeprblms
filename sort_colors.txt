class Solution:
    def sortColors(self, nums: List[int]) -> None:
        c = 0
        for i in range(len(nums)):
            if nums[c] == 0:
                nums.pop(c)
                nums.insert(0, 0)
                c += 1
            elif nums[c] == 2:
                nums.pop(c)
                nums.append(2)
            else:
                c += 1
        return
