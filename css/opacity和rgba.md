它们都是用来设置透明度的

- opacity：取值从0到1，0是透明，1不透明
- rgba：R红色、G绿色、B蓝色、a透明度，rgb可以取正整数或百分数，a是从0-1

区别：

​	主要区别是继承性的问题，opacity会被子代继承，rgba则不会给子代继承

​	例如：大盒子内有小盒子，如果给大盒子设置opacity，则小盒子也会有opacity效果，但是rgba不会

根据需要选择使用哪种