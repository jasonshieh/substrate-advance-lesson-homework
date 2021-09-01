# Substrate 进阶班作业

姓名:谢小件 </br>
学号:45 </br>
所在小组:TEAM3 </br>

## 第一课作业

验证命令
```sh
cd project/substrate-node-template
cargo test --package pallet-poe
```

第一题:编写存证模块的单元测试代码，包括：
* [创建存证的测试用例](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/poe/src/tests.rs#L6)
* [撤销存证的测试用例](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/poe/src/tests.rs#L36)
* [转移存证的测试用例](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/poe/src/tests.rs#L72) *

第二题:创建存证时，为存证内容的哈希值 Vec
* [设置长度上限，超过限制时返回错误](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/poe/src/lib.rs#L73)
* [并编写测试用例](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/poe/src/tests.rs#L14)*

## 第二课作业

验证命令
```sh
cd project/substrate-node-template
cargo test --package pallet-kitties
```

1: 增加[买](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/lib.rs#L170)和[卖](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/lib.rs#L158)的extrinsic,对视频中kitties的实现进行重构，[提取出公共代码](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/lib.rs#L198) </br>
2: KittyIndex[不在pallet中指定](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/lib.rs#L29)，而是[在runtime里面绑定](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/runtime/src/lib.rs#L284) </br>
3: 测试代码能测试所有的五个方法，[能检查所有定义的event，能测试出所有定义的错误类型](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/tests.rs) </br>
4. 引入Balances里面的方法，[在创建时质押一定数量的token](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/lib.rs#L92)，[在购买时支付token](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/substrate-node-template/pallets/kitties/src/lib.rs#L182)。*

## 第三课作业
```sh
链启动
cd project/kitties/node
cargo build --release
./target/debug/node-template --dev --tmp
前端启动
cd frontend
yarn install
yarn start
```

1.能查询出链上[猫咪总数](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/kitties/frontend/src/Kitties.js#L43) <br/>
2.能查询出链上[猫咪的 ID, 所属主人，及其 DNA](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/kitties/frontend/src/Kitties.js#L33) <br/> 
3.能在 react 端[组合回需要的数组结构](https://github.com/jasonshieh/substrate-advance-lesson-homework/project/kitties/frontend/src/Kitties.js#L33) <br/>