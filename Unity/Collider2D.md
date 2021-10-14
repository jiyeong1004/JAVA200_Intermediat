# Collider2D 컴포넌트

- 2차원 공간에서 오브젝트의 충돌 범위를 나타내는 컴포넌트
- 충돌 범위의 생김새나 특징에 따라 "OO Collider 2D" 와 같이 이름을 명명함
    
    - Box Collider 2D
        
        특징 : 사각형 범위의 충돌 범위
        
        < 변수 >
        
        - Offset : 충돌 범위 중심점
        - Size : 충돌 범위 크기
    - Circle Collider 2D
        
        특징 : 원 범위의 충돌 범위. 연산 속도가 가장 빠름.
        
        < 변수 >
        
        - Offset : 충돌 범위 중심점
        - Radius : 충돌 범위 반지름 크기
    - Edge Collider 2D
        
        특징 : 점의 개수, 각 점의 위치를 설정할 수 있기 때문에 다양한 곡선 형태로 충돌 범위 표현 가능 (주로 2D 게임의 바닥 충돌에 사용)
        
        < 변수 >
        
        - Offset : 충돌 범위 중심점
        - Edge Radius : 충돌 선의 두께
        - Points : 선을 이루는 점의 개수와 각 점의 위치
    - Polygon Collider 2D
        
        특징 : 텍스처의 모양과 비슷한 형태로 충돌 범위 생성 (Edge와 마찬가지로 Points 수정 가능)
        
        < 변수 >
        
        - Offset : 충돌 범위 중심점
        - Points : 선을 이루는 점의 개수와 각 점의 위치
    - Capsule Collider 2D
        
        특징 : 캡슐 모양의 충돌 범위 생성 (사람 형태의 캐릭터에 주로 사용)
        
        < 변수 >
        
        - Offset : 충돌 범위 중심점
        - Size : 충돌 범위 크기
        - Direction : 둥근 캡슐이 표현되는 방향 (Vertical : 위 / 아래, Horizontal : 좌 / 우)
    - Composite Collider 2D
        
        특징 : 다른 게임 오브젝트의 Collider 2D들을 하나로 묶어주는 역할
        (Box Collider 2D, Polygon Collider 2D만 가능)
        
        < 사용 >
        
        1-1. 빈 게임오브젝트 생성
        
        1-2. 생성한 게임오브젝트에 Composite Collider 2D 컴포넌트 추가
        (Rigidbody2D 컴포넌트가 함께 추가된다.)
        
        2. 하나로 묶고 싶은 Collider 2D 컴포넌트를 가지고 있는 게임오브젝트들을 Composite Collider 2D 컴포넌트를 가지고 있는 게임오브젝트의 자식 오브젝트로 설정
        
        3. 자식 오브젝트들의 Collider 2D 컴포넌트에 있는 "Used By Composite" 변수 활성화
        

- Material : 해당 오브젝트의 마찰력 등을 설정할 수 있는 물리 메터리얼 등록 가능
- Is Trigger : 활성화 되면 오브젝트가 충돌되지 않고 뚫고 지나간다.
- Offest : 충돌 범위 중심점 위치
- Size : 충돌 범위 크기