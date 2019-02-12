/*
* @Author: Zhang Guohua
* @Date:   2019-02-12 17:22:11
* @Last Modified by:   zgh
* @Last Modified time: 2019-02-12 17:22:36
* @Description: create by zgh
* @GitHub: Savour Humor
*/
# Canvas

## 全局操作

- 清空画布： 清空绘制内容， 通过 bg.clearRect 清除，实际是将区域变为透明。下次使用 bg.fill 扔会展示出来。 canvas 每当宽，高重新设置时，会自动清空画布内容。