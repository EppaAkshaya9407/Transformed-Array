# Transformed-Array
def constructTransformedArray(nums):
    n=len(nums)
    result=[0]*n
   for i in range(n):
        if nums[i]==0:
            result[i]=0
        elif nums[i]>0:
            index=(i+nums[i])%n
            result[i]=nums[index]
        else:
            index=(i+nums[i])%n
            result[i]=nums[index]
    return result
n=int(input("Enter number of elements:"))
nums=list(map(int,input("Enter elements:").split()))
result=constructTransformedArray(nums)
print("Transformed array:",result)
