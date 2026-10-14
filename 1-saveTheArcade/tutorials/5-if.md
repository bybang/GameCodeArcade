# If

<!-- Modified by bybang on 2026-10-15: Korean localization of instructional prose and verified deployed @hideDone directive. Original: Cleverlike-MakeCode/GameCodeArcade, 1-saveTheArcade/tutorials/5-if.md, commit 2b7a616a1212cbf9992450213c62b8d0bdfffd0b. Licensed under Apache-2.0; see LICENSE. -->

### @explicitHints 1

### @activities true

### @hideDone true

## 첫 번째 활동

### 판단하기

어떤 문제에서는 동작을 계속 반복해야 하지만, 모든 동작을 매번 똑같이 반복해야 하는 것은 아닙니다. ``||logic:if||`` 블록은 특정 동작을 언제 수행할지 판단하여 코드를 간단하게 만들 수 있습니다.
``||logic:if||`` 블록도 **compound statement block**의 한 종류입니다. **condition**을 사용하여 코드를 실행할지 판단합니다. condition이 true이면 ``||logic:if||`` 블록 안의 코드가 실행됩니다.

#### ~ tutorialhint

**condition**은 true 또는 false가 될 수 있습니다. **condition block**은 끝이 뾰족한 모양이어서 condition이 필요한 자리에 들어간다는 것을 알 수 있습니다.

### Agent detect

``||logic:if||`` 블록과 ``||agent:agent detect||`` 블록을 사용하여 ``||agent:agent destroy||``가 단단한 블록만 부수게 해 보세요.
``||logic:LOGIC||`` 카테고리에서 ``||logic:if||`` 블록을 끌어와 ``||loops:repeat||`` 블록 안에 넣으세요.
``||agent:AGENT||`` 카테고리에서 ``||agent:agent detect||`` 블록을 끌어와 ``||logic:if||`` 블록 안에서 모양이 맞는 자리에 넣으세요.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
        }
    }
})
```
### condition 설정하기

Agent가 바라보는 방향을 기준으로 오른쪽을 확인하도록 ``||agent:agent detect||`` 블록의 드롭다운 메뉴를 설정하세요. ``||agent:agent detect||`` 블록은 Agent 옆에 단단한 블록이 있는지 판단할 수 있습니다.
``||agent:agent detect||`` 블록에서 방향을 올바르게 지정했는지 확인하세요. ``||loops:repeat||`` 블록의 반복 횟수는 이미 올바르게 설정되어 있습니다.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
           
        }
        
    }
})
```

### If true...

Agent가 ``||agent:agent detect||``로 오른쪽에서 블록을 감지하면, ``||agent:agent destroy||``로 그 블록을 부수게 하려고 합니다. ``||logic:if||`` 블록 안에 ``||agent:agent destroy||``를 넣고 방향을 **right**로 설정하세요.
Agent가 부술 블록을 **감지하든 감지하지 못하든**, 이 과정이 끝나면 앞으로 이동해야 합니다. ``||agent:agent move||``의 방향을 **forward**로 설정하여 ``||logic:if||`` 블록 다음에 추가하세요.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.destroy(RIGHT)
        }
        agent.move(FORWARD, 1)
    }
})
```

### 코드 실행하기

초록색 **Play** 버튼을 눌러 코드를 실행하세요. 그런 다음 채팅에 **fix**를 입력하여 Agent가 작업을 완료하게 하세요.

condition이 있는 코드는 특정 코드 구간을 실행할지 판단할 수 있으므로, 모든 단계를 일일이 코드로 작성할 필요가 없습니다.

#### ~ tutorialhint

```blocks
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.destroy(RIGHT)
        }
        agent.move(FORWARD, 1)
    }
})
```

```template
player.onChat("fix", function () {
    for (let index = 0; index < 12; index++) {
    }
})
```

```ghost
player.onChat("run", function () {
    for (let index = 0; index < 12; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
            agent.move(FORWARD, 1)
        }
    }
})
```
