# moment-token

제품 UI용 디자인 토큰 모음입니다. 색상, 여백(spacing), 반경(radius), 타이포그래피(primitives)와 의미론적(semantic) 디자인 변수들을 포함합니다.

이 패키지는 웹 애플리케이션에서 사용하기 위한 생성된 CSS 변수, SCSS 변수, Tailwind v4 테마 토큰 및 원본 토큰 JSON 파일들을 내보냅니다.

## 설치

```bash
npm install @kindtiger/moment_token
```

## 패키지 내보내기 (exports)

```js
import '@kindtiger/moment_token/css';
import '@kindtiger/moment_token/scss';
import '@kindtiger/moment_token/tailwind';
```

원본 JSON 토큰 파일을 직접 가져다 쓸 수도 있습니다:

```js
import colors from '@kindtiger/moment_token/tokens/color---semantic.json';
```

## 제공되는 출력물

- CSS 변수: `@kindtiger/moment_token/css`
- SCSS 변수: `@kindtiger/moment_token/scss`
- Tailwind v4 테마: `@kindtiger/moment_token/tailwind`
- 원본 토큰 파일: `@kindtiger/moment_token/tokens/*`

## 사용 예시

### CSS

```css
@import '@kindtiger/moment_token/css';

.card {
  background: var(--color-surface-default);
  color: var(--color-text-primary);
  border-radius: var(--radius-md);
  padding: var(--spacing-4);
}
```

### SCSS

```scss
@use '@kindtiger/moment_token/scss' as *;

.card {
  background: $color-surface-default;
  color: $color-text-primary;
  border-radius: $radius-md;
  padding: $spacing-4;
}
```

### Tailwind CSS

```css
@import 'tailwindcss';
@import '@kindtiger/moment_token/tailwind';
```

Tailwind v4에서 제공하는 생성된 테마 변수를 통해 디자인 토큰을 사용할 수 있습니다.

## 포함된 토큰 그룹

- 색상 (Colors)
  - 원시 색상(primitive)
  - 의미적 토큰(브랜드, 표면, 텍스트, 배지 등)
- 여백 (Spacing)
- 반경 (Radius)
- 타이포그래피 (Typography)
  - 폰트 크기
  - 행간(line-height)
  - 자간(letter-spacing)
  - 폰트 패밀리

## 원본 및 빌드

이 패키지는 `tokens/` 디렉터리의 JSON 토큰 파일들에서 Style Dictionary를 사용해 생성됩니다.

```bash
npm run build
```

빌드 스크립트: `node build-tokens.mjs` (package.json의 `build` 스크립트 참조)

배포 전에는 `npm run build` 또는 `npm publish` 전에 자동 실행되는 `prepublishOnly` 훅이 동작합니다.

## 라이선스

MIT

## 저장소

https://github.com/simseonbeom/moment-token
