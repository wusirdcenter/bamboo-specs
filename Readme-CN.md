# bamboo

>  交易撮合系统

[英文](./README.md)

## bamboo是什么
- bamboo旨在整合filecoin的生态资源，建立一个面向用户的filecoin web3.0存储交易撮合市场门户网站（这有别于lotus的实现，lotus做了各类市场的协议级实现，而bamboo则为面向用户的各类市场的应用级实现），让用户便捷地全面获取链上以及链下的信息源。
	- 竞拍市场
	- 存储市场
	- 检索市场
	- 公证市场
- 任意人通过运行bamboo
- bamboo的设计初衷是一个不可篡改的系统，其具备web3.0的可信任特性。
	- bamboo会使用[web3db](https://github.com/mingzhutek/web3db-specs)，一个基于ipfs设计的带状态的数据库。
	- 通过打通以太坊智能合约进行信任源设计，来保证bamboo的可信任度。
	- 补充持久化在交易过程中，所需要的链下信息。

## 设计框架

![](./img/arch.png)

## 组成
- [Database](./database/Readme.md)
	- 持久化
	- 状态树设计
- 可信源
	- 通过以太坊智能合约
- [Model](./model/Readme.md)主要对系统参与方的抽象，包括终端用户角色，系统角色。
	- 角色
		- 客户
		- 存储矿工
		- 检索矿工
		- 公证人
		- 系统角色（用于自动交易时的代理授权等）
	- 市场 
		- 竞拍市场
		- 存储市场
		- 检索市场
		- 公证市场
- [Logic](./logic/Readme.md)为具体的交互逻辑类模块
- [API](./api/Readme.md)
	- http
	- rpc
- 用户交互
  - cli
  - front-end网站

## 实施
- 后端实现
  - golang
  - typscript
- 前端实现
  - react