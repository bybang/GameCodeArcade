# Agent 조작하기

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/2-3-events.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### Sequencing

``||player:on chat command||`` 안에 여러 동작을 넣으면 Agent가 다양한 일을 순서대로 수행하게 할 수 있습니다. Agent에는 여러 기능이 있으며, 드롭다운 메뉴에서 설정을 바꿀 수 있습니다.

**interact**라는 이름의 ``||player:on chat command||`` 안에 ``||agent:agent move||`` 블록이 이미 들어 있습니다. 여기에 Agent가 레버를 조작하는 동작도 필요합니다.

#### ~ tutorialhint

**next**를 눌러 튜토리얼을 계속 진행하세요.

### Agent interact

``||agent:agent interact||`` 블록은 ``||agent:AGENT||`` 카테고리에 있으며, Agent가 레버, 버튼, 문, 울타리 문 등의 장치를 조작하게 합니다.

``||agent:AGENT||`` 카테고리에서 ``||agent:agent interact||`` 블록을 끌어와 ``||agent:agent move||`` 블록 아래에 놓으세요. 두 블록 모두 **interact** ``||player:on chat command||`` 안에 있어야 합니다.

#### ~ tutorialhint

```blocks
player.onChat("interact", function () {
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
})
```

### 복습

초록색 Play 버튼을 눌러 Agent가 새 chat command를 사용할 수 있게 하세요. Minecraft 채팅에 **interact** 명령을 입력하면 **interact** ``||player:chat command||`` 안의 코드가 실행됩니다.

#### ~ tutorialhint

```blocks
player.onChat("interact", function () {
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
})
```

```template
player.onChat("interact", function () {
    agent.move(FORWARD, 1)
})
```
