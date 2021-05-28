# 2.Kth-smallest-element-

(a) USING MIM-HEAP

import heapq
from heapq import heappop
class Solution:
    def kthSmallest(self,arr, l, r, k):
        '''
        arr : given array
        l : starting index of the array i.e 0
        r : ending index of the array i.e size-1
        k : find kth smallest element and return using this function
        '''
        heapq.heapify(arr)
        
        while k > 1:
            heappop(arr)
            k = k-1
        return arr[0]
