# Repeat

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/4-repeat.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### 패턴

어떤 문제를 해결하려면 정해진 동작들을 계속 반복해야 합니다. **repeat loop**를 사용하면 같은 코드를 여러 번 작성할 필요가 없어 해결 방법이 간단해집니다.
``||loops:repeat||`` 블록은 **compound statement block**입니다. compound statement block은 statement block이 들어갈 수 있는 곳이면 어디든 들어갈 수 있으며, 안쪽에도 statement block을 더 넣을 수 있는 공간이 있습니다.

#### ~ tutorialhint

``||loops:repeat||`` 블록은 event block 안에 넣을 수 있지만, 그 안에도 statement block을 넣어야 합니다.

```blocks
player.onChat("clean", function () {
    for (let index = 0; index < 4; index++) {
    	
    }
})
```

### 동작 순서 반복하기

``||loops:repeat||`` 블록을 ``||loops:LOOPS||`` 카테고리에서 끌어와 ``||player:chat command||`` 안에 넣고, 기존의 ``||agent:agent destroy||``와 ``||agent:agent move||`` 코드 블록을 그 안에 넣으세요.

``||loops:repeat||`` 블록은 같은 코드 구간을 여러 번 반복해서 실행하므로 **loop**의 한 종류입니다.

#### ~ tutorialhint

```blocks
player.onChat("clean", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```

### Loop 반복 횟수

``||loops:repeat||`` 블록을 몇 번 실행할지 지정해야 합니다. 기본값은 4번이지만, Agent가 청소해야 할 칸은 12칸입니다. ``||loops:repeat||`` 블록 안의 **4**를 **12**로 바꿀 수 있습니다.

#### ~ tutorialhint

```blocks
player.onChat("clean", function () {
    for (let index = 0; index < 12; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```

### 복습

repeat loop는 일련의 statements를 정해진 횟수만큼 실행합니다. loop를 사용하면 문제를 해결하기 위해 작성해야 하는 코드의 양을 크게 줄일 수 있습니다.

Play를 누른 다음 채팅에 **clean**을 입력하여 코드를 실행하는 것을 잊지 마세요.

#### ~ tutorialhint

```blocks
player.onChat("clean", function () {
    for (let index = 0; index < 12; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```

```template
player.onChat("clean", function () {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
})
```

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
