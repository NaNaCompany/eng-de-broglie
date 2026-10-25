# 드브로이 파장 계산기

입자 운동량으로 물질파 파장 계산

- Plan ID: E059
- App: https://nanalab.kr/eng-de-broglie/
- Repository: https://github.com/NaNaCompany/eng-de-broglie
- Formula: `λ = h/p`
- Output: 드브로이 파장 λ

## Model

p>0. 입력은 운동량 크기다. 속력을 운동량으로 자동 환산하지 않으므로 상대론 운동량 여부는 입력자가 정한다. 파동함수·위치 불확도는 계산하지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `6.62607015e-10`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
