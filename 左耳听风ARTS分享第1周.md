@[TOC](左耳听风ARTS分享第1周)

> 每周完成一个ARTS： 每周至少做一个 leetcode的算法题、阅读并点评至少一篇英文技术文章、学习至少一个技术技巧、分享一篇有观点和思考的技术文章。（也就是Algorithm、Review、Tip、Share 简称ARTS）

## Algorithm
两数之和
给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。
你可以假设每种输入只会对应一个答案。但是，你不能重复利用这个数组中同样的元素。

    var twoSum = function(nums, target) {
          var record = [];
           for(let i = 0 ; i < nums.length ; i ++)
                record[nums[i]]= i;
    
       for(let i = 0 ; i < nums.length; i ++){
    
                let index = record[target - nums[i]];
                if(index != null && index != i){
                    let res = [i, index];
                    return res;
                }
            }
            return "the input has no solution";
    };

## Review
[The Key To Accelerating Your Coding Skills](http://blog.thefirehoseproject.com/posts/learn-to-code-and-be-self-reliant/)

感悟：编程是一种终身学习体验，是一个不断挑战自己的过程，应该努力每天超出自己的极限，寻找超出当前技能的问题来建立和扩展技能，产生学会一切的感觉只意味着应该开始考虑解决更复杂的问题。

## Tip
[https://hexo.io/zh-cn/docs/](https://hexo.io/zh-cn/docs/)
使用hexo搭建个人博客网站

## share
[学习笔记：输入url到页面渲染的整个过程](https://blog.csdn.net/hyqapple/article/details/88907597)
