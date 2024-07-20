# Sorting Algorthms Cheat Sheet

## Bubble Sort:
Time: O($N^2$)\
Space: O(1)

```
func sortArray(_ nums: [Int]) -> [Int] {
        var nums = nums
        for i in 0 ..< nums.count - 1{
            for k in 0 ..< nums.count - 1{
                var swapped = false
                if nums[k] > nums[k+1] {
                    nums.swapAt(k, k+1)
                    swapped = true
                }
            }
            if !swapped {return nums}
        } 
        return nums
    }
```
Comment: Bubble sort works by comparing two adjacent numbers and switching them if the one on the right is smaller than the one on the left.

## Selection Sort:
Time: O($N^2$)\
Space: O(1)

```
func sortArray(_ nums: [Int]) -> [Int] {
        var nums = nums
        for i in 0 ..< nums.count {
            var (min, idx) = (nums[i], i)
            for k in i ..< nums.count {
                if min > nums[k] {
                    min = nums[k] 
                    idx = k
                }
            }
            nums.swapAt(i, idx)
        }
        return nums
    }
```
Comment: Starting at index 0, we find the smallest element to the right of the array and swap it with the starting index. Repeat the process with the new starting index being the previous+1.

## Insertion Sort:
