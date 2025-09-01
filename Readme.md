27.移除元素 使用两指针向中间移动的方式，在指针指向同一个，指向末尾时出错，于是用if特定判断解决；
while(nums[last]==val)last--保证了后端指针指向非删除的元素，减少了循环次数

35.搜索插入位置，思路需要二分法查找，
mid = ((right - left) >> 1) + left;保证了不溢出，且位运算更快

66.加一 需要分类关注 digits 的末尾出现了多少个 9 即可

121.买卖股票的最佳时机 暴力法会超时，需要一次遍历寻找可能的差价
使用了prices[i+1]<price[i]作为条件计算差价，节省了计算资源

125.验证回文串
学习了isalnum(ch) tolower(ch) b(a.rbegin(), a.rend())对字符处理的函数
 while (left < right) {
           if (sgood[left] != sgood[right]) {
                return false;
            }
            ++left;
            --right;  }两指针向中间方法

136.只出现一次的数字 需要思路：使用异或运算，任何数和 0 做异或是自己，任何数和其自身异或是0，异或运算满足交换律和结合律

387.字符串中的第一个唯一字符 没用哈希表和队列，用了2个循环，在指针指向同一个，指向末尾时出错，于是用if特定判断解决；

2942.查找包含给定字符的单词 学习定义数组和添加元素方法：vector<int> res; if (words[i].find(x) != string::npos)  res.push_back(i);

