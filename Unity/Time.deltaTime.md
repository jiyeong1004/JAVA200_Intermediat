# Time.deltaTime

- 이전 Update() 종료부터 다음 Update() 시작까지의 시간 (업데이트 사이의 시간)
    
    ex) 1분(60초)에 Update()가 60번 호출된다면 Time.deltaTime은 1
    
- 사양이 좋지 않은 컴퓨터는 60초에 Update()가 60번 호출
    - Time.deltaTime의 값은 1

- 사양이 좋은 컴퓨터는 60초에 Update()가 120번 호출
    - Time.deltaTime의 값은 0.5
    

이동거리 = 방향(Direction) * 속도(Speed) * Time.deltaTime

- 두 컴퓨터에서 캐릭터 이동을 했을 때
    - 캐릭터의 Update() 1회 당 이동거리를 5m 라고 할 때
    - 사양이 좋지 않은 컴퓨터는 60초에 Update()가 60회 호출
    - 사양이 좋은 컴퓨터는 60초에 Update()가 120회 호출

사양이 좋지 않은 컴퓨터 : 5m * 60회 * 1 = 300m

사양이 좋은 컴퓨터 : 5m * 120회 * 0.5 = 300m

Tip. 계산의 편의를 위해 60초에 60번이라고 얘기를 했지만 FPS 60 일 때 초당 60회 호출이라는 뜻