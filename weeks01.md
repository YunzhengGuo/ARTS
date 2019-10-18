极客时间《左耳听风》专栏ARTS活动打卡第 1周。

> 1.Algorithm: 每周至少做一道LeetCode算法题 
> 2.Review: 阅读并点评至少一篇英文技术文章 
> 3.Tip: 学习至少一个技术技巧 
> 4.Share: 分享一篇有观点和思考的技术文章

A

给定两个大小为 m 和 n 的有序数组 nums1 和 nums2。

请你找出这两个有序数组的中位数，并且要求算法的时间复杂度为 O(log(m + n))。

你可以假设 nums1 和 nums2 不会同时为空。

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/median-of-two-sorted-arrays
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

```python

class Solution:
    def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
        m = len(nums1)
        # print(m)
        n = len(nums2)
        # if m > n :#长的是nums2
        #     nums1 , nums2 = nums2, nums1
        for i in nums2:
            nums1.append(i)
        nums1 = sorted(nums1)
        # print(nums1)
        #定义中位数  数位置标签
        if (m+n)%2 == 0:
            median_pos_1, median_pos_2 = (m+n)/2,(m+n)/2+1  #在列表中实际位置需要减一，从零开始计数
            median_num1 = nums1[int((m+n)/2-1)]
            median_num2 = nums1[int((m+n)/2)]
            print(f'median_pos1:{median_pos_1} \nmedian_pos2:{median_pos_2}')
            print("是偶数")#10/2=5,5+1#中位数是 第五个 第5+1个
            median_num = (median_num1+median_num2)/2.0
        else:
            median_pos_1 = int((m+n)/2+0.5)
            median_num = nums1[median_pos_1-1]
            print(f'pos1:{median_pos_1}')
            print("是奇数")#5/2+0.5 中位数是第2.5+0.5个
        return float(median_num)
```

R

 使用Tensorflow进行对象检测 

 https://towardsdatascience.com/playing-with-object-detection-8f116ec0ce4d 

T

python paramiko  用这个库做了个文件传输和远程控制服务器的脚本

S

机器学习重要概念理解

 https://mp.weixin.qq.com/s?__biz=MzI2NjkyNDQ3Mw==&mid=2247488363&idx=1&sn=b26305adbb71d48b234165fc37457c10&chksm=ea87ebbdddf062ab55217c251894d8047a6779fe0bdadff70ac548c87c2a22d8f28a80127588&token=594238315&lang=zh_CN&scene=21#wechat_redirect 

