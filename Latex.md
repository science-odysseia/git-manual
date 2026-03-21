# LATEX 수식 

<details>
<summary> <h2> 0. 수식 기본 표기법 </h2> </summary>

수식 기본 표현 : 양 끝에 **띄어쓰기 없이** $를 붙인다.

    $a + b = c$

$a + b = c$

이 경우 한줄만 작성가능. 여러줄을 쓰려 할 경우 오류가 날 수 있음.

여러 줄을 작성할 경우 아래와 같이 `$$` `$$` 로 덮어주면 된다.

아래와 같이 하면 중앙에 식이 생긴다.

    $$
    a + b = c
    $$

또는 엔터 없이

    $$ a + b = c $$

$$
a + b = c
$$

다만 md상의 도표 안에서 `$$` `$$`은 사용 불가하니 조심.

</details>

<details>
<summary> <h2> 1. 기본연산자 </h2> </summary>

## 기본연산자

|기본연산자|수식표현|결과|
|:---:|:---:|:---:|
|덧셈| `a + b` |$a + b$|
|뺄셈| `a - b` |$a - b$|
|곱셈| `a \cdot b`, `a \times b`|$a \cdot b$, $a \times b$|
|나눗셈| `\frac{분자}{분모}` |$\frac{분자}{분모}$|
|지수| `a^b` | $a^b$ | 
|아래첨자| `a_n`, `a_{xy}` | $a_n$, $a_{xy}$ |
|루트| `\sqrt{x}`, `\sqrt[n]{x}` = `x ^ (1/n)` | $\sqrt{x}$, $\sqrt[3]{x}$ |
|같음| `=` | $=$ |
|같지 않음| `\neq` | $\neq$ |
|근사| `\approx` | $\approx$ |
|초과, 미만| `>`, `<` | $>$, $<$ |
|이상, 이하| `\ge`, `\le` | $\ge$, $\le$ |

</details>

<details>
<summary> <h2> 2. 삼각/로그함수 </h2> </summary>

## 삼각/로그 함수
|함수|코드|
|:---:|:---:|
|$\sin x$|`\sin x`|
|$\cos x$|`\cos x`|
|$\tan x$|`\tan x`|
|$\log x$|`\log x`|
|$\log_a x$|`\log_a x`|
|$\ln x$|`\ln x`|

</details>

<details>
<summary> <h2> 3. 괄호표기 </h3> </summary>

## 괄호 표기
| 왼쪽 괄호 | 표기 | 오른쪽 괄호 | 표기 |
|:---:|---|:---:|---|
| $\left( \right.$ | `\left(` | $\left. \right)$ | `\right)` |
| $\left\\{ \right.$ | `\left\\{` | $\left. \right\\}$ | `\right\\}` |
| $\left[ \right.$ | `\left[` | $\left. \right]$ | `\right]` |

`{`만 `\\{`로 입력하자.

참고로 라텍스 문법은 괄호 짝이 맞지 않으면 에러난다.

만약 한쪽 괄호만 사용하고 싶다면

`\left.`, `\right.` 처럼 `.`을 이용하면 된다.

</details>

<details>
<summary> <h2> 4. 그리스 문자 표기법 </h2> </summary>

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

</details>

<details>
<summary> <h2> 5. 합/곱/적분표기법 </h2> </summary>

## 합/곱/적분

|코드|결과|디스플레이 모드|결과|
|---|---|---|---|
|`\sum_{i=1}^{n} a_n`|$\sum_{i=1}^{n} a_n$|`$\displaystyle \sum_{i=1}^{n} a_n$`|$\displaystyle \sum_{i=1}^{n} a_n$|
|`$\prod_{i=1}^{n} b_n$`|$\prod_{i=1}^{n} b_n$|`$\displaystyle \prod_{i=1}^{n} b_n$`|$\displaystyle \prod_{i=1}^{n} b_n$|
|`$\int_{a}^{b} f(x)$`|$\int_{a}^{b} f(x)$|`$\displaystyle \int_{a}^{b} f(x)$`|$\displaystyle \int_{a}^{b} f(x)$|

</details>

<details>
<summary> <h2> 6. 미분표기법 </h2> </summary>

## 미분표기법

1차미분

    \frac{d}{dx} f(x)
    \frac{df}{dx}

$\frac{d}{dx} f(x)$

$\frac{df}{dx}$

n차미분

    \frac{d^n f}{dx^n}

$\frac{d^n f}{dx^n}$

편미분

    \frac{\partial f}{\partial x}

$\frac{\partial f}{\partial x}$


</details>

<details>
<summary> <h2> 7. 필요, 충분, 필요충분조건 화살표 활용법 </h2> </summary>

## 화살표 활용

$\to$

    \to
    \rightarrow

$a \to b$, $a \rightarrow b$

$\Rightarrow$, $\Leftarrow$

    \Rightarrow
    \Leftarrow

$a \Rightarrow b$, $a \Leftarrow b$

$\leftrightarrow$

    \leftrightarrow

$a \leftrightarrow b$

</details>

<details>
<summary> <h2> 8. 극한표기법 </h2> </summary>

## 극한

|코드|결과|디스플레이 모드|결과|
|---|---|---|---|
|`\lim_{x \to \infty} f(x)`|$\lim_{x \to \infty} f(x)$|`$\displaystyle \lim_{x \to \infty} f(x)$`|$\displaystyle \lim_{x \to \infty} f(x)$|

\#\# 참고 : `\infty` : $\infty$

</details>

<details>
<summary> <h2> 9. 조건분할식 </h2> </summary>

## 조건식
무조건 `$$` `$$` 구문으로 쓸 것. `$` `$`로 쓰면 인식 못할 확률 큼.

    $$ \begin{cases} x^2 & x > 0 \\\\ 0 & x \le 0 \end{cases} $$

$$ \begin{cases} x^2 & x > 0 \\\\ 0 & x \le 0 \end{cases} $$

</details>

<details>
<summary> <h2> 10. 벡터 표기법 </h2> </summary>

## 벡터 기호 표시

    \vec{v}

$\vec{v}$

여러 글자 벡터
    \overrightarrow{ABCDEFG}

$\overrightarrow{ABCDEFG}$

</details>

<details>
<summary> <h2> 11. 행렬표기법 </h2> </summary>

## 행렬

대괄호 (bmatrix)

    $$ \begin{bmatrix} 1 & 2 & 3 \\\\ 4 & 5 & 6 \end{bmatrix} $$

$$ \begin{bmatrix} 1 & 2 & 3 \\\\ 4 & 5 & 6 \end{bmatrix} $$

소괄호(pmatrix)

    $$ \begin{pmatrix} x \\\\ y \end{pmatrix} $$

$$ \begin{pmatrix} x \\\\ y \end{pmatrix} $$

행렬식(vmatrix)

    $$ \det(A) = \begin{vmatrix} a & b \\\\ c & d \end{vmatrix} $$

$$ \det(A) = \begin{vmatrix} a & b \\\\ c & d \end{vmatrix} $$

행렬에서 ... 표시 방법
`\cdots` : $\cdots$
`\vdots` : $\vdots$
`\ddots` : $\ddots$

    $$
    \mathbf{A} = \begin{bmatrix}
    a_{11} & \cdots & a_{1n} \\
    \vdots & \ddots & \vdots \\
    a_{m1} & \cdots & a_{mn}
    \end{bmatrix}
    $$

$$
\mathbf{A} = \begin{bmatrix}
a_{11} & \cdots & a_{1n} \\
\vdots & \ddots & \vdots \\
a_{m1} & \cdots & a_{mn}
\end{bmatrix}
$$

</details>