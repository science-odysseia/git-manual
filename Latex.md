# LATEX 수식 

수식 기본 표현 : 양 끝에 **띄어쓰기 없이** $를 붙인다.

    $a + b = c$

$a + b = c$

아래와 같이 하면 중앙에 식이 생긴다.

    $$
    a + b = c
    $$

$$
a + b = c
$$

## 기본연산자

|기본연산자|수식표현|결과|
|:---:|:---:|:---:|
|덧셈| `a + b` |$a + b$|
|뺄셈| `a - b` |$a - b$|
|곱셈| `a \cdot b`, `a \times b`|$a \cdot b$, $a \times b$|
|나눗셈| `\frac{분자}{분모}` |$\frac{분자}{분모}|
|지수| `a^b` | $a^b$ | 
|아래첨자| `a_n`, `a_{xy}` | $a_n$, $a_{xy}$ |
|루트| `sqrt{x}`, `sqrt[n]{x}` = `x ^ (1/n)` | $\sqrt{x}$, $\sqrt[3]{x}$ |

## 삼각/로그 함수
|함수|코드|
|---|---|
|$\sin x$|`\sin x`|
|$\cos x$|`\cos x`|
|$\tan x$|`\tan x`|
|$\log x$|`\log x`|
|$\log_a x$|`\log_a x`|
|$\ln x$|`\ln x`|

## 괄호 표기
| 왼쪽 괄호 | 표기 | 오른쪽 괄호 | 표기 |
|---|---|---|---|
| $\left( \right.$ | `\left(` | $\left. \right)$ | `\right)` |
| $\left\\{ \right.$ | `\left\\{` | $\left. \right\\}$ | `\right\\}` |
| $\left[ \right.$ | `\left[` | $\left. \right]$ | `\right]` |

`{`만 `\\{`로 입력하자.

참고로 라텍스 문법은 괄호 짝이 맞지 않으면 에러난다.

만약 한쪽 괄호만 사용하고 싶다면

`\left.`, `\right.` 처럼 `.`을 이용하면 된다.


## 그리스 문자 표기

|그리스 문자(소문자)|코드|그리스문자(대문자)|코드(대문자)|
|:---:|:---:|:---:|:---:|
|$\alpha$|`\alpha`|\-|\-|
|$\beta$|`\beta`|\-|\-|
|$\gamma$|`\gamma`|$\Gamma$|`\Gamma`|
|$\delta$|`\delta`|$\Delta$|`\Delta`|
|$\epsilon$|`\epsilon`|\-|\-|
|$\zeta$|`\zeta`|\-|\-|
|$\eta$|`\eta`|\-|\-|
|$\iota$|`\iota`|\-|\-|
|$\kappa$|`\kappa`|\-|\-|
|$\lambda$|`\lambda`|$\Lambda$|`\Lambda`|
|$\mu$|`\mu`|\-|\-|
|$\nu$|`\nu`|\-|\-|
|o(Omicron)|`o`|\-|\-|
|$\pi$|`\pi`|$\Pi$|`\Pi`|
|$\rho$|`\rho`|\-|\-|
|$\sigma$|`\sigma`|$\Sigma$|`\Sigma`|
|$\tau$|`\tau`|\-|\-|
|$\upsilon$|`\upsilon`|$\Upsilon$|`\Upsilon`|
|$\phi$|`\phi`|$\Phi$|`\Phi`|
|$\chi$|`\chi`|\-|\-|
|$\psi$|`\psi`|$\Psi$|`\Psi`|
|$\omega$|`\omega`|$\Omega$|`\Omega`|

## 합/곱/적분

|코드|결과|디스플레이 모드|결과|
|---|---|---|---|
|`\sum_{i=1}^{n} a_n`|$\sum_{i=1}^{n} a_n$|`$\displaystyle \sum_{i=1}^{n} a_n$`|$\displaystyle \sum_{i=1}^{n} a_n$|
|`$\prod_{i=1}^{n} b_n$`|$\prod_{i=1}^{n} b_n$|`$\displaystyle \prod_{i=1}^{n} b_n$`|$\displaystyle \prod_{i=1}^{n} b_n$|
|`$\int_{a}^{b} f(x)$`|$\int_{a}^{b} f(x)$|`$\displaystyle \int_{a}^{b} f(x)$`|$\displaystyle \int_{a}^{b} f(x)$|

## 극한

|코드|결과|디스플레이 모드|결과|
|---|---|---|---|
|`\lim_{x \to \infty} f(x)`|$\lim_{x \to \infty} f(x)$|`$\displaystyle \lim_{x \to \infty} f(x)$`|$\displaystyle \lim_{x \to \infty} f(x)$|

\#\# 참고 : `\infty` : $\infty$
