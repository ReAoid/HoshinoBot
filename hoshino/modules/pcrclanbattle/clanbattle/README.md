# PCR会战管理

v2.0 🐒也会用的会战管理

[toc]

## 特色

- 简洁灵活，学习简单
- 预约Boss，自动提醒
- 一键催刀，警察减负
- 全角半角，繁简均可


## 快速开始

0. 与维护组联系<del>(py)</del>，邀请bot入群

1. 群初次使用时，需要设置公会名与服务器地区，使用命令 `!建会 N<公会名> S<服务器地区>` 

    ```
    !建会 Nリトルリリカル Sjp
    !建会 N小小甜心 Stw
    !建会 N今天版号批了吗 Scn
    ```

2. 使用命令 `!入会 <昵称>` 进行注册

    ```
    !入会 祐树
    ```

3. 使用命令 `!出刀 <伤害值>` 上报伤害

   ```
   !出刀 514w
   !收尾
   !出补时刀 114w
   ```

4. 忙于工作/学习/娱乐时，使用命令 `!预约 <Boss号>` 预约出刀

    ```
    !预约 5
    ```

5. 不慎失误时，使用命令 `!挂树` 等待救援

    ```
    !挂树
    ```

6. 夜深人静时，使用命令 `!催刀` 在群内at未出刀的成员，督促出刀

    ```
    !催刀
    ```



## Hoshino会战管理命令一览
### 使用前必读

> 💡 会战系命令均以感叹号`!`开头，半全角均可  
> 💡 命令与参数之间**必须**以*空格*隔开  
> 💡 `X<参数名>`表示参数以字母`X`引导，使用时需输入`X`，无需输入尖括号`<>`  
> 💡 `()`包括的参数为可选

### 公会管理命令

| 使用场景 | 命令格式      | 备注           | 使用例      |
| -------- | ------------- | -------------- | ----------- |
| 初次使用 | `!建会 N<公会名> S<服务器地区>` | 日服jp，台服tw，<del>国服cn</del> | `!建会 Nリトルリリカル Sjp`<br/>`!建会 N小小甜心 Stw`<br/>`!建会 N今天版号批了吗 Scn` |
| 成员注册 | `!入会 <昵称>` |  | `!入会 祐树` |
| 成员注册<br/>*管理拉人* | `!入会 @<qq号> <昵称>` | 可直接@ 需本人/管理/群主 | `!入会 @1802002609 N祐树` |
| 成员查看 | `!查看成员` |  | `!查看成员` |
| 成员除名 | `!退会 (@<qq号>)` | 可直接@ 需本人/管理/群主 | `!退会` |
| 成员清空 | `!清空成员` | 需管理/群主 | `!清空成员` |
| 批量注册 | `!一键入会` | 需管理/群主，群员少于40时可用 | `!一键入会` |

> 如需修改公会名/服务器地区，再次使用`!建会`命令  
> 如需修改昵称，再次使用`!入会`命令

-----

### 出刀记录命令

| 使用场景         | 命令格式               | 备注                       | 使用例                 |
| :--------------- | :--------------------- | :------------------------- | :--------------------- |
| 伤害上报         | `!出刀 <伤害值>`         | 支持以w或k作为单位         | `!出刀 600w`             |
| 伤害上报<br/>*收尾* | `!出尾刀`     | 自动计算伤害；亦可手动指定 | `!出尾刀`             |
| 伤害上报<br/>*补偿时间* | `!出补时刀 <伤害值>` | 支持以w或k作为单位         | `!出补时刀 100w`        |
| 伤害上报<br/>*代打* | `!出刀 <伤害值> Q<qq号>` | 可直接@                    | `!出刀 500w @1802002609` |
|伤害补报<br/>*指定周目/Boss*|`!出刀 <伤害值> R<周目数> B<Boss编号>`|尾刀/补时刀使用`!出尾刀`/`!出补时刀`|`!出刀 500w R4 B2`|
| 掉线记录         | `!掉刀`                  | 记录伤害为0，本日余刀减1 | `!掉刀`                  |
| 删除记录         | `!删刀 E<记录编号>`      | 群管理可删除他人记录       | `!删刀 E42`              |

> **名词解释**  
> 💡**尾刀**：队伍首次出击，并击败Boss的刀  
> 💡**补时刀**：用补偿时间出的刀

> ⚠️若用**补时刀**击败Boss则无更多补偿时间，此时应报**补时刀**而非<del>*尾刀*</del>

-----

### 预约及锁定Boss命令

| 使用场景              | 命令格式             | 备注               | 使用例        |
| :-------------------- | :------------------- | :----------------- | :------------ |
| 预约Boss     | `!预约 <Boss号> M<留言>` | 到达Boss时自动提醒 | `!预约 1 M哥布林杀手参上` |
| 预约取消     | `!预约取消 <Boss号>` |                    | `!预约取消 1` |
| 预约查询     | `!预约查询`          |                    | `!预约查询`   |
| 清空预约队列 | `!预约清空 <Boss号>` | 需管理/群主        | `!预约清空 4` |
| 锁定Boss | `!锁定` | 公会全体成员均需**自觉**使用<br/>注：锁定对报刀无强制约束力，不使用本功能也不影响报刀<br/> | `!锁定` |
| 解锁Boss | `!解锁` | 报刀时自动解锁 | `!解锁` |



-----

### 等待救援命令

| 使用场景            | 命令格式           | 备注                           | 使用例                                         |
| :------------------ | :----------------- | :----------------------------- | :--------------------------------------------- |
| 失误挂树   | `!挂树`            | Boss斩杀后自动提醒             | `!挂树`                                        |
| <del>取消挂树</del> | <del>`!下树`</del> | *防止被恶意使用，不可主动下树* | ~~你下尼🐴呢？<br/>🌳不是玩具！<br/>给👴🏻老实挂着~~ |

-----

### 查询/统计命令

| 使用场景 | 命令格式 | 备注                                 | 使用例  |
| :------- | :------- | :----------------------------------- | :------ |
| 进度查询 | `!进度`  | 查看会战攻略进度                     | `!进度` |
| 统计分数 | `!统计`  | 统计本月会战分数                     | `!统计` |
| 余刀查询 | `!查刀`  | 查看成员余刀数，已下班成员不会被列出 | `!查刀` |
| 一键催刀 | `!催刀`  | 群内at催刀，需管理/群主              | `!催刀` |

