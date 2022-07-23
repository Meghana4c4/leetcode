class Solution:
    def isValid(self, s: str) -> bool:
        d={')':'(','}':'{',']':'['}
        l=[]
        for i in s:
            if len(l)>0 and l[-1]==d.get(i,False):
                l.pop(-1)
            else:
                l.append(i)
        if len(l)==0:
            return True
        return False

