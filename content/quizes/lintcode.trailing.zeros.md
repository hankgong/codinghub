+++
title = "Trailing Zeros"
draft = false
date = "2017-09-07"
Tags = ["Q-Math", "Q-Easy"]
Categories = ["LintCode"]
+++

Number of 5s + number of 5x5s + number of 5x5x5...

{{< highlight python "linenos=inline,hl_lines=1 2">}}
class Solution:
    # @param n a integer
    # @return ans a integer
    def trailingZeros(self, n):
        ret = 0
        div = 5
        r = n/div
        
        while r > 0:
            r = n/div
            div *= 5
            ret += r
            
        return ret
{{< /highlight >}}