# While

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/6-while.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### condition을 사용하는 loop

loop가 필요한 문제 중에는 ``||loops:repeat block||``이 가장 적합한 방법이 아닌 경우도 있습니다. 특정 condition이 충족될 때까지 코드를 실행해야 할 수도 있습니다.

``||loops:while||`` 블록은 condition을 사용하여 안의 코드를 계속 반복할지 판단하는 또 다른 종류의 loop입니다.

#### ~ tutorialhint

``||loops:while||`` 블록은 condition이 true인 동안 코드를 실행합니다. 안의 코드를 실행한 뒤에는 ``||loops:while||`` 블록이 condition을 다시 확인하여 코드를 한 번 더 실행할지 판단합니다. condition이 false가 되면 ``||loops:while||`` loop가 종료됩니다.

### Agent inspect

``||agent:agent inspect||`` 블록은 value block입니다. **value block**은 둥근 모양이며, **value**라고 부르는 정보를 제공합니다. ``||agent:agent inspect||``가 반환하는 정보는 Agent 옆에 있는 Minecraft 블록의 종류입니다. value block은 다른 코드 블록에서 value가 필요한 둥근 입력칸에 들어갑니다. ``||agent:agent inspect||``가 ``||agent:agent set block or item||`` 블록의 둥근 입력칸에 들어 있는 것을 살펴보세요.

#### ~ tutorialhint

``||agent:agent inspect||``를 ``||agent:agent set block or item||`` 안에 넣으면 Agent의 오른쪽에 있는 블록이 무엇이든 그 블록을 Agent의 인벤토리에 넣습니다.

### value 비교하기

``||logic:LOGIC||`` 카테고리에는 두 value를 비교하는 ``||logic:comparison||`` condition block이 있습니다. **equal sign (=)**을 선택하면 ``||logic:comparison||`` 블록은 두 value가 같을 때 true를 반환합니다.
``||logic:comparison||`` 블록을 사용하여 ``||loops:while||`` 블록의 condition을 만들어 보세요. Agent는 ``||loops:while||``을 사용하여, ``||agent:agent inspect||``의 방향을 **down**으로 설정하여 확인한 블록이 **cobblestone**과 같은 동안 작업을 계속해야 합니다.

#### ~ tutorialhint

```blocks
player.onChat("copy", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE) {
        agent.setItem(agent.inspect(AgentInspection.Block, RIGHT), 1, 1)
        agent.place(LEFT)
        agent.move(FORWARD, 1)
    }
})
```

### 복습

``||loops:while||`` 블록은 condition을 사용하여 코드를 계속 반복할지 판단합니다. ``||loops:While||`` loop는 반복 횟수는 명확하지 않지만 반복을 계속할 condition이 명확할 때 유용합니다. ``||logic:Comparison||`` 블록은 두 value를 비교하여 condition을 만들 수 있습니다.
코드를 실행하고 채팅에 **copy**를 입력하는 것을 잊지 마세요.

#### ~ tutorialhint

```blocks
player.onChat("copy", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE) {
        agent.setItem(agent.inspect(AgentInspection.Block, RIGHT), 1, 1)
        agent.place(LEFT)
        agent.move(FORWARD, 1)
    }
})
```

```template
player.onChat("copy", function () {
    while (false) {
        agent.setItem(agent.inspect(AgentInspection.Block, RIGHT), 1, 1)
        agent.place(LEFT)
        agent.move(FORWARD, 1)
    }
})
```

```ghost

player.onChat("copy", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) == COBBLESTONE) {
        agent.setItem(agent.inspect(AgentInspection.Block, FORWARD), 1, 1)
        agent.place(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
