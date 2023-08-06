```python
# Falta mejorar
# Los ultimos elementos de la lista no importan
def removerDuplicados(nums: list[int]) -> int:
    k = 0
    if(len(nums) == 1):
        print(nums)
        return 1
    if(len(nums) == 0):
        print(nums)
        return 0  
    if(len(nums) == 2):       
        if(nums[0] == nums[1]):
            print(nums)
            return 2
        else:
            print(nums)
            return 3
    
    for j in range(0, len(nums)-1):
        if(j == len(nums)-1):
            break
        if(nums[j] != nums[j+1]):
            k+=1
            continue
        elif(j+1 == len(nums)-1 ):
            k+=1
            continue  
        elif(nums[j+2] == nums[j+1]):
            if(j+2 == len(nums)-1 ):
                del nums[j+2]
                k+=1
            else:
                val = nums[j+2]
                while(nums[j+2] == val):   
                    del nums[j+2]
                
                k+=2
 
    print(nums)
    return k+1
            
```

