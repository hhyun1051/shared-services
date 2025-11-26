# Home Assistant Shared Service

Team-H 프로젝트를 위한 Home Assistant 설치.

## 설치

```bash
cd /root/shared-services/home-assistant
docker compose up -d
```

## 접속

- URL: http://localhost:8123
- 초기 설정 시 사용자 계정 생성

## SmartThings 연동

1. Home Assistant UI 접속
2. Settings → Devices & Services
3. Add Integration 클릭
4. "SmartThings" 검색
5. Samsung 계정으로 로그인 (OAuth 자동)
6. 장치 자동 임포트

## API Token 생성 (Team-H 연동용)

1. Profile (좌측 하단) 클릭
2. Security 탭
3. Long-Lived Access Tokens 섹션
4. Create Token 클릭
5. Token 이름: "team-h-manager-i"
6. 생성된 token을 `/root/team-h/.env`에 추가:
   ```
   HOMEASSISTANT_URL=http://localhost:8123
   HOMEASSISTANT_TOKEN=your_long_lived_token_here
   ```
