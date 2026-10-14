# Agent 조작하기

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/2-1-events.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### Chat commands

``||player:on chat command||`` event block은 Minecraft 채팅 창으로 특정 메시지를 보내면 그 안의 코드를 실행합니다. 채팅에 **move**를 입력하여 ``||agent:agent move forward||`` 블록으로 Agent를 한 블록 앞으로 이동시켜 보세요.
초록색 Play 버튼을 눌러 코드를 실행하세요. 그런 다음 **T** 키를 누르거나 채팅 아이콘을 눌러 Minecraft 채팅 창을 열고 **move**를 입력하세요.

#### ~ tutorialhint

```blocks
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```

```template
player.onChat("move", function () {
    agent.move(FORWARD, 1)
})
```
