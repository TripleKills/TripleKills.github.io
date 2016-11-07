---
layout: post
title: 超人2应用宝接入
category: 超人2
tags: 
keywords: 
description: 
---
##相关信息
	APPID： 1105774050

##官方文档地址
[官方文档](http://wiki.open.qq.com/wiki/YSDK介绍)

##官方流程图
![流程图](http://og9k4sqik.bkt.clouddn.com/%E5%BA%94%E7%94%A8%E5%AE%9D%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)

###H5YSDK支付接口调用
	<script src="http://qzs.qq.com/open/mobile/h5gamesdk/build/sdk.js"></script>
    /**
     * H5YSDK支付接口调用
     * @param  {Object}     opt             传入参数
     * @param  {number}     opt.saveValue   默认充值数量 填0/null/""的时候唤起提案数量的界面
     * @param  {number}     opt.zoneId      充值的大区
     * @param  {Function}   opt.onError     错误回调  
     * @example opt.onError = function(ret){
     *                          if(ret.code == -1){
     *                              //ios环境
     *                          }else if(ret.code == -2){
     *                              //非应用宝环境
     *                          }else if(ret.code == -3){
     *                              //midas正在下载中。。。。
     *                          }else if(ret.code == -4){
     *                              //当前应用宝版本过低，请更新应用宝
     *                          }else if(ret.code == -5){
     *                              //支付插件初始化中
     *                          }else if(ret.code == -6){
     *                              //充值失败，稍后重请试
     *                          }else if(ret.code == -7){
     *                              // 参数不正确
     *                          }
     *                      }                                       
     * @param  {Function}   opt.onSuccess   成功回调                                                                            
     * */
    H5YSDK.requestPay({
        saveValue:1,
        zoneId:"1",
        onError:function(ret){
            console.log(ret);
        }
    });
