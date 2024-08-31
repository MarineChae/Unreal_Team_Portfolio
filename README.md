## Brutal Takedown Squad

* 제작기간 : 2024.02.02 ~ 2024.03.29

* 개발환경 : C++, UnrealEngine 5

* 시연 영상 : https://youtu.be/iBa4doPBSXI?si=GzZfLKTNEdRT6OjO&t=510
  
* DownloadLink :http://naver.me/5DjEcInA



![Alt text](readImage/Lobby.png)
![Alt text](readImage/s1.png)

<br>

## AI

 * EvadeGranade
   - 수류탄과 AI 캐릭터의 방향을 이용하여 수류탄으로 부터 도망가게 구현했습니다.
  ![Alt text](readImage/s1.png)

 * ChasePlayer
   - 플레이어가 AI의 시야반경 내에 들어오게 되면 공격하고 그 후 플레이어의 위치를 TargetLocation으로 저장 후 추후에 플레이어가 시야에서 사라진 경우 추적할 수 있게 구현했습니다.
   ![Alt text](readImage/s1.png)

 * Patrol Target Locatin
   - 플레이어가 시야에서 사라진 경우 마지막으로 발견한 위치에서 탐색하도록 구현했습니다.

  * Away From Player
    - AI의 체력이 일정 수준 이하로 체력이 감소하면 Hidable 태그가 있는 액터 뒤로 이동하여 플레이어로 부터 숨도록 구현했습니다.
    - 숨은 이후 잠시 대기 후 다시 전투에 참여합니다.

  * Patrol Random Location
    - EQS를 사용하여 AI캐릭터 주변으로 부터 가장 먼 거리를 선별하여 랜덤하게 이동합니다.
    - 구조물에 막히는 경우 거리가 멀어도 선별되지 않습니다.

## Level Design


## Interactive Object

  * Interactive Object Interface
     - 상호작용이 가능한 오브젝트들을 만들기위해 인터페이스를 구현하였습니다.
      
      
    

  * C4
    - 타이머 이벤트를 사용하여 일정시간 키다운 유지 시 함정이 해제되게 구현했습니다.
    - 키다운을 중지 하거나 플레이어의 시선을 돌리는 경우 타이머가 중단 및 초기화 됩니다.
    - 폭탄이 터지는 경우 폭탄에서 플레이어로 라인트레이싱을 진행 후 플레이어와 함정 사이의 다른 구조물이 있는경우 데미지를 경감 시켰습니다.
    - AI는 함정에 걸리지 않도록 태그를 활용하여 플레이어가 아닌경우 함정이 발동하지 않습니다.
  



