# Sequencing

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/3-sequencing.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### 블록 놓기

Agent는 Minecraft 블록을 놓을 수 있지만, 그러려면 여러 단계를 거쳐야 합니다. Agent가 Minecraft 블록을 놓으려면 먼저 인벤토리에 블록이 있어야 합니다.

첫 번째 단계는 ``||agent:agent set block or item||``을 사용하여 Agent의 인벤토리에 블록을 넣는 것입니다.

#### ~ tutorialhint

Agent는 기본적으로 인벤토리의 첫 번째 슬롯에 있는 블록을 놓습니다. 따라서 ``||agent:agent set block or item||``을 사용하여 Agent의 인벤토리 **1**번 슬롯에 블록을 넣으세요.

### 블록 이름으로 검색하기

``||agent:agent set block or item||``의 드롭다운 메뉴에는 항목이 많아서 특정 Minecraft 블록을 찾기가 어려울 수 있습니다.

드롭다운 메뉴에서 **redstone**을 검색하면 **Block of Redstone**을 빠르게 찾아 선택할 수 있습니다.

#### ~ tutorialhint

```blocks
player.onChat("place", function () {
    agent.setItem(REDSTONE_BLOCK, 1, 1)
})
```

### 연속된 statements

Agent의 인벤토리에 블록을 넣은 다음, 두 번째 단계는 ``||agent:agent place||``로 Agent가 그 블록을 놓게 하는 것입니다.

``||agent:agent place||`` 블록을 ``||agent:AGENT||`` 카테고리에서 끌어와 ``||agent:agent set block or item||`` 아래에 연결하세요. 그런 다음 **place** ``||player:chat command||``를 실행하세요.


#### ~ tutorialhint

```blocks
player.onChat("place", function () {
    agent.setItem(REDSTONE_BLOCK, 1, 1)
    agent.place(FORWARD)
})
```

```template
player.onChat("place", function () {
    agent.setItem(GRASS, 1, 1)
})
```

```ghost
player.onChat("run", function () {
    agent.setItem(REDSTONE_BLOCK, 1, 1)
    agent.place(FORWARD)
})
```
