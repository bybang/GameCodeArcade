# Agent 조작하기

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/2-2-events.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### Agent destroy

``||agent:AGENT||`` 카테고리를 열고 ``||agent:agent destroy||`` 블록을 **destroy**라는 이름의 ``||player:on chat command||`` 블록 안으로 끌어다 놓으세요.

Agent가 앞을 가로막는 블록을 부수게 해 보세요. Minecraft 채팅에 **destroy** 명령을 입력하면 **destroy** ``||player:on chat command||`` 안의 코드가 실행됩니다.


#### ~ tutorialhint


```blocks
player.onChat("destroy", function () {
    agent.destroy(FORWARD)
})
```

```template
player.onChat("destroy", function () {
	
})
```
