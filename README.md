# pixiv-server-SDK

[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

**🌟 一个能够轻松获取Pixiv的插画数据的SDK**

**🌟 An SDK that can easily get Pixiv illustration data."**




## Table of Contents

- [pixiv-server](#pixiv-server)
  - [Table of Contents](#table-of-contents)
  - [Install](#install)
  - [Usage](#usage)
      - [RPixiv 类](#RPixiv 类)
  - [API](#api)
      - [getDayRanks(range ?: string)](getDayRanks(range ?: string))
      - [getWeekRanks(range ?: string)](getWeekRanks(range ?: string))
      - [getMonthRanks(range ?: string)](getMonthRanks(range ?: string))
  - [Maintainers](#maintainers)
  - [License](#license)

## Install

```shell
# npm
npm install runtu-pixiv-sdk
# yarn
yarn add runtu-pixiv-sdk

```

## Usage

### RPixiv 类

* SDK以`RPixiv`类的形式出现，你需要从包中导出类。
* 同时该类可以传递一个`AxiosProxy`参数以便于你使用代理进行Pixiv请求。
* "The SDK appears in the form of the `RPixiv` class, and you need to export the class from the package."
* Additionally, `RPixiv` can receive an param called `AxiosProxy`, allowing you to use a proxy for Pixiv requests.
```typescript
import { RPixiv } from 'runtu-pixiv-sdk'

const pixiv = new RPixiv(proxy)

/**
proxy: {
	host: string,
	port: number
}
*/
```

* `AxiosProxy`更多的类型请参考 [AxiosProxy](http://www.axios-js.com/zh-cn/docs/#axios-options-url-config-1)
* `AxiosProxy`: Please refer to [AxiosProxy](http://www.axios-js.com/zh-cn/docs/#axios-options-url-config-1) for more types.



## API
#### getDayRanks(range ?: string)
* 获取Pixiv每日的插画排行榜数据。
* Get Pixiv daily monthly illustration ranking data

```typescript
await pixiv.getDayRanks("2022-11-11")
```

#### getWeekRanks(range ?: string)
* 获取Pixiv每周的插画排行榜数据。
* Get Pixiv weekly illustration ranking data

````typescript
await pixiv.getWeekRanks("2022-11-14")
````



#### getMonthRanks(range ?: string)
* 获取Pixiv每月的插画排行榜数据。
* Get Pixiv weekly monthly ranking data

```typescript
await pixiv.getMonthRanks("2022-11-14")
```

> 后续接口还在移植中



## Maintainers

[@Runtus](https://github.com/Runtus)

## License

MIT © 2022 Runtus
