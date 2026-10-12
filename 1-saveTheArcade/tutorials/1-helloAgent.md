# Hello, Agent.

<!-- Modified by bybang on 2026-10-11: Korean localization of instructional prose only. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/1-helloAgent.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### Events

``||loops:on start||`` 블록은 **event block**입니다. event block은 특정 event가 발생하면 그 안의 코드를 실행합니다.

``||loops:on start||`` 블록에서는 Play 버튼을 누르는 것이 이 event block을 실행하는 event입니다.

#### ~ tutorialhint

**event block**은 다른 코드 블록을 안에 넣을 수 있는 모양입니다.

### Statements

``||player:say||`` 블록은 **statement block**입니다. statement block은 동작을 수행합니다.

``||player:say||`` 블록에는 "Hello, Agent."라는 텍스트가 들어 있습니다. Play 버튼을 눌러 코드를 실행하고 채팅에 텍스트를 표시해 보세요.

#### ~ tutorialhint

**statement block**은 event block 안에 넣을 수 있는 모양입니다.

### 복습

``||player:say||`` 블록을 ``||loops:on start||`` 블록 안에 넣고 Play 버튼을 누르면 Minecraft 채팅으로 메시지가 전송됩니다.

#### ~ tutorialhint

```blocks
player.say("Hello, Agent.")
```

```template
player.say("Hello, Agent.")
```
