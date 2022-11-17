# 云开发 quickstart

这是云开发的快速启动指引，其中演示了如何上手使用云开发的三大基础能力：

- 数据库：一个既可在小程序前端操作，也能在云函数中读写的 JSON 文档型数据库
- 文件存储：在小程序前端直接上传/下载云端文件，在云开发控制台可视化管理
- 云函数：在云端运行的代码，微信私有协议天然鉴权，开发者只需编写业务逻辑代码

## 参考文档

- [云开发文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/basis/getting-started.html)
# 云开发 返回码介绍

请求成功 返回200
数据为空时返回201
参数错误返回400


<!--  
第一个参数是 提交的数据，第二个是接口路径，第三个是修改的id 
PostRequest用，更新数据时候调用，
await wx.api.PostRequest(data, 'updateUser', this.data._id); 
	async updateUser(data) {
		const result = await wx.api.PostRequest(data, 'updateUser', this.data._id);
		if (result.code) {
			wx.showToast({
				title: '更新成功',
			})
			console.log(result, '更新用户资料成功');
		}
	},

第一个参数是 添加的数据上传到数据库，第二个是接口路径，
await wx.api.AllRequest(data, 'getUser');
AllRequest和getRequest用于添加数据、获取数据的时候调用，
	async updateUser(data) {
		const result = await wx.api.PostRequest(data, 'getUser', this.data._id);
		if (result.code) {
			wx.showToast({
				title: '更新成功',
			})
			console.log(result, '更新用户资料成功');
		}
	},
-->
