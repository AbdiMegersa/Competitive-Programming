class Solution:
    def hIndex(self, citations: List[int]) -> int:

        cit = [-i for i in citations]

        heapq.heapify(cit)

        res = 0
        i = 1
        while i <= len(citations):
            val = heapq.heappop(cit)

            if -val < i:
                break
            else:
                res = i
            i += 1
        
        return res
