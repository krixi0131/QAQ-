# QAQ-
```python
a=str(input())
ma=0
pre,suf=[0]*len(a),[0]*len(a)
n=len(a)
for i in range(len(a)):
    if i==0:
        if a[i]=="Q":
            pre[i]=1
        else:
            pre[i]=0
        continue
    if a[i]=="Q":
        pre[i]=pre[i-1]+1
    else:
        pre[i]=pre[i-1]
for i in range(len(a)-1,-1,-1):
    if i==len(a)-1:
        if a[i]=="Q":
            suf[i]=1
        else:
            suf[i]=0
        continue
    if a[i]=="Q":
        suf[i]=suf[i+1]+1
    else:
        suf[i]=suf[i+1]    
for i in range(len(a)-1):
    if a[i]=="A":
        ma+=pre[i]*suf[i+1]
print(ma)
 ```
