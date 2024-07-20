***Sorting Algorthms Cheat Sheet

Bubble sort:
Time: O(N^2)
Space: O(N)
```
func sortArray(_ nums: [Int]) -> [Int] {
        var nums = nums
        for i in 0 ..< nums.count - 1{
            for k in 0 ..< nums.count - 1{
                if nums[k] > nums[k+1] {
                    nums.swapAt(k, k+1)
                }
            }
        } 
        return nums
    }
```
