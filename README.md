# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

本项目实现了一个仿b站评论区的功能，核心源码来自黑马程序员的React18入门到实战系列课程，感谢黑马提供的资源，祝黑马越办越好
本项目基于黑马的源代码进行了一系列优化使得功能更加完善，具体优化如下
1.新增count变量来记录评论数，实现了评论数动态改变而非原有的固定值
2.将点赞功能按钮化，实现真正的点赞功能
3.对评论日期进行改进，将时间精确到秒并制防止错误
4.对评论排序算法进行了优化，以往排序算法的主要问题有排序时间精度不够只能到分钟级别，同一分钟内的评论顺序会出现错误；每次新增评论后无法实现自动排序，需要重新切换Type才可以实现排序；在最热排序下直接点赞无法正确按照点赞数排序。使用useMemo进行性能优化，来保证每次commonList和Typey以及flag变化时候都会进行重排（flag用于标记点赞数是否发生变化）
