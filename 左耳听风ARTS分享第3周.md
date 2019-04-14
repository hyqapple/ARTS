@[TOC](左耳听风ARTS分享第3周)

> 每周完成一个ARTS： 每周至少做一个 leetcode的算法题、阅读并点评至少一篇英文技术文章、学习至少一个技术技巧、分享一篇有观点和思考的技术文章。（也就是Algorithm、Review、Tip、Share 简称ARTS）

## Algorithm
169.求众数
给定一个大小为 n 的数组，找到其中的众数。众数是指在数组中出现次数大于 ⌊ n/2 ⌋ 的元素。

你可以假设数组是非空的，并且给定的数组总是存在众数。

示例 1:

输入: [3,2,3]
输出: 3

示例 2:

输入: [2,2,1,1,1,2,2]
输出: 2
**解法1：**

        var majorityElement = function(nums) {
        let count = 1;
		let maj = nums[0];
		for (let i = 1; i < nums.length; i++) {
			if (maj == nums[i])
				count++;
			else {
				count--;
				if (count == 0) {
					maj = nums[i + 1];
				}
			}
		}
		return maj;
};
![求众数](https://img-blog.csdnimg.cn/2019041117074912.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2h5cWFwcGxl,size_16,color_FFFFFF,t_70)
**解法2：**

    var majorityElement = function(nums) {
        nums.sort(function(a,b){return a-b});
    		return nums[parseInt(nums.length / 2)];
    };
![求众数](https://img-blog.csdnimg.cn/20190411174347494.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2h5cWFwcGxl,size_16,color_FFFFFF,t_70)
## Review
[JUnit Best Practices](http://www.kyleblaney.com/junit-best-practices/)

这篇文章详细介绍了单元测试的流程。大体分为以下几点：

 1. 确保单元测试只在内存中运行，不要有http请求或者与数据库、文件服务器进行交互，太慢或者太不可靠。
 2. 使用最合适的断言方法，以正确的顺序放置断言参数，使用包含正在测试的方法和条件的约定来命名单元测试
 3. 确保测试类与测试中的生产类存在于同一Java包中，不要在单元测试中打印任何东西。
 4. 不要在单元测试类构造函数中初始化; 请改用@Before方法，不要在测试类中使用静态成员，不要编写自己的catch块。在测试类中，不要声明方法抛出任何特定类型的异常，不要在单元测试中使用Thread.sleep。

## Tip
[Vue.js 技术揭秘/](https://ustbhuangyi.github.io/vue-analysis/)


## share
[学习笔记：关于前后端调试程序](https://blog.csdn.net/hyqapple/article/details/89188431)

