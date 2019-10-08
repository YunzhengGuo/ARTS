极客时间《左耳听风》专栏ARTS活动打卡第1周。

> 1.Algorithm: 每周至少做一道LeetCode算法题 
> 2.Review: 阅读并点评至少一篇英文技术文章 
> 3.Tip: 学习至少一个技术技巧 
> 4.Share: 分享一篇有观点和思考的技术文章

A

给定 n 个非负整数 a1，a2，...，an，每个数代表坐标中的一个点 (i, ai) 。在坐标内画 n 条垂直线，垂直线 i 的两个端点分别为 (i, ai) 和 (i, 0)。找出其中的两条线，使得它们与 x 轴共同构成的容器可以容纳最多的水

```python

def maxArea(height):
    max_area = 0
    length = len(height)
    i = 0
    j = length-1
    if length<=1:
        return 0
    while i<j:
        width = j-i
        max_area = max(min(height[i], height[j])*width, max_area)#先计算后“交换”
        print(f'left: {height[i]} right{height[j]} max_area{max_area}')
        if height[i]<height[j]:
            i = i+1
        else:
            j=j-1
     return max_area
```

R

来自medium的BeautifulSoup的小教程

https://medium.com/free-code-camp/how-to-scrape-websites-with-python-and-beautifulsoup-5946935d93fe

T

基于tensorflow的手写数字识别训练手动实现与理解

S

非常实用的opencv学习小教程

http://ex2tron.wang/

