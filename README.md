# Growth Radar · 하이스트비뇨기과

하이스트비뇨기과와 `doctor.jmj`, `예작`, `프라움`의 광고·키워드·콘텐츠 기회를 한 화면에서 기록하고, GEO·E-E-A-T·마케팅 실행까지 연결하는 정적 대시보드입니다.

## 실행

`index.html`을 브라우저에서 바로 열거나, 폴더에서 아래 명령으로 로컬 서버를 실행하세요.

```powershell
python -m http.server 4173
```

이후 `http://127.0.0.1:4173/`에 접속합니다.

## 사용 흐름

1. **경쟁사 광고**에서 Meta Ad Library에서 확인한 소재와 집행 기간을 기록합니다.
2. **키워드 기회**에서 검색량·경쟁도·현재 순위를 입력합니다. 점수가 높은 주제가 우선 노출됩니다.
3. **콘텐츠 큐**에서 광고 신호와 SEO 기회를 콘텐츠 아이디어로 관리합니다.
4. **수집 로그**에 Meta Ads·Naver·Search Console 확인 이력을 남깁니다.
5. 우측 상단 `↥` 버튼으로 현재 데이터를 JSON으로 백업할 수 있습니다.

## GEO·마케팅 분석

- **GEO 진단**: URL·브랜드·업종과 관찰 가능한 신호로 Citability·Authority·E-E-A-T·Technical·Schema를 결정론적으로 계산합니다.
- **마케팅 분석**: 환자 검색 의도, 경쟁사 메시지, 하이스트의 콘텐츠·랜딩·전환 액션을 연결합니다.
- **BYOK**: 상단 `BYOK`에서 각 사용자가 자신의 AI 키를 브라우저에 저장할 수 있습니다. 키는 저장소나 코드에 기록하지 않습니다.

레퍼런스 해석과 설계 원칙은 [docs/REFERENCE_ANALYSIS.md](docs/REFERENCE_ANALYSIS.md), [docs/GEO_ARCHITECTURE.md](docs/GEO_ARCHITECTURE.md), [docs/EEAT_EVIDENCE_MATRIX.md](docs/EEAT_EVIDENCE_MATRIX.md), [docs/MARKETING_ANALYSIS.md](docs/MARKETING_ANALYSIS.md), [docs/SITE_BASELINE.md](docs/SITE_BASELINE.md)에 정리했습니다.

데이터는 브라우저의 `localStorage`에 저장됩니다. 현재 버전은 외부 서비스 API를 직접 호출하지 않으므로, 실제 자동 수집을 붙이려면 Meta Ad Library·네이버 키워드 도구·Search Console API와 GEO 스냅샷 수집기 연동이 다음 단계입니다.

## GitHub Pages 배포

저장소의 `main` 브랜치에 push하면 `.github/workflows/pages.yml`이 정적 파일을 GitHub Pages에 배포합니다. GitHub 저장소 설정에서 Pages의 Source를 **GitHub Actions**로 선택하세요.

현재 공개 주소: https://notoow.github.io/growth-radar/

정적 Pages에서는 서버 비밀키를 숨길 수 없습니다. 따라서 실측용 키는 개인별 브라우저 BYOK로만 사용하거나, 별도 백엔드/Actions Secret에서 호출하는 구조를 권장합니다.
