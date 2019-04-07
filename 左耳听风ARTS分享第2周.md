@[TOC](左耳听风ARTS分享第2周)

> 每周完成一个ARTS： 每周至少做一个 leetcode的算法题、阅读并点评至少一篇英文技术文章、学习至少一个技术技巧、分享一篇有观点和思考的技术文章。（也就是Algorithm、Review、Tip、Share 简称ARTS）

## Algorithm
15.三数之和
给定一个包含 n 个整数的数组 nums，判断 nums 中是否存在三个元素 a，b，c ，使得 a + b + c = 0 ？找出所有满足条件且不重复的三元组。

注意：答案中不可以包含重复的三元组。

        var threeSum = function(nums) {
        nums.sort(function(a,b){return a-b})
        res =[]
         for (let i = 0; i < nums.length - 2; i++) {
            if (i == 0 || (i > 0 && nums[i] != nums[i - 1])){
                l = i+1
                r = nums.length-1
                while (l < r){
                    s = nums[i] + nums[l] +nums[r]
                    if (s ==0){
                        res.push([nums[i],nums[l],nums[r]])
                        while (l < r && nums[l] == nums[l+1]) l += 1
                        while (l < r && nums[r] == nums[r-1]) r -= 1
                        l +=1
                        r -=1
                    }
                    else if (s>0){
                        while (l < r && nums[r] == nums[r - 1]) {r--;}
                       r -=1 
                    }
                    else {
                         while (l < r && nums[l] == nums[l + 1]) {l++;}
                        l +=1
                    }
                }
            }
         }
        return res
    };
![threesum](https://img-blog.csdnimg.cn/20190407163739215.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2h5cWFwcGxl,size_16,color_FFFFFF,t_70)
## Review
[How To Ask Questions The Smart Way](http://www.catb.org/~esr/faqs/smart-questions.html)

感悟：我们所提技术问题的解答很大程度上取决于你提问的方式与解决此问题的难度，文章讲述了如何提问才更有可能得到满意的答复。大体分为以下几点：

 1. 提问前先自己尝试通过互联网，阅读手册，“常见问题文档”（FAQ）熟人等方式查询问题，并仔细检查代码语句，用清晰、语法、拼写正确的语句书写。
 2. 提问时寻找合适（专业对口，参与者多等）的论坛或其他渠道。
 3. 当项目存在开发者邮件列表时，要向列表而不是其中的个别成员提问，发邮件使用“对象──偏差”（式的描述），在“对象”部分指明是哪一个或哪一组东西有问题，在“偏差”部分则描述与期望的行为不一致的地方。
 4. 使用易于读取且标准的文件格式发送问题
 5. 描述问题应准确且有内容，描述问题的症状，问题发生的环境，提问前做过的研究及其理解，提问前为确定问题而采取的诊断步骤，最近对计算机或软件配置的任何相关改变，如果可能，提供在可控环境下重现问题的方法；描述问题应该精炼且有内容。
 6. 除非真的有把握不要下断言，不要低声下气，要描述问题症状而不是猜测，在开头就描述你的目标，然后才陈述遇到问题的特定步骤。并在最后加上礼貌用语。
 7. 如果受到到嘲讽式的回答，不要抱怨，也不要卷进口水战中。
 8. 授人以鱼，不如授人以渔
 9. 对初学者抱有宽容之心
 10. 如果不确定，一定要说出来！

## Tip
[http://md.aclickall.com/](http://md.aclickall.com/)
Markdown排版利器，支持 "一键排版" 、自定义css、80多种代码高亮。
能让Markdown内容，无需作任何调整就能一键复制到微信公众号、博客园、掘金、知乎、csdn、51cto、wordpress、hexo。。。等平台。

## share
[学习笔记：前端性能优化](https://blog.csdn.net/hyqapple/article/details/88964049)

