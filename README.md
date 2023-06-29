# React-Cookie

리액트 쿠키를 사용하는 방법은 매우 쉽다. 

```
"react-cookie": "^4.1.1",
npm install react-cookie
```

의존성 주입을 받고

```ts
import { Cookies } from 'react-cookie';

const cookies = new Cookies();

export const setCookie = (name: string, value: string, option?: any) => {
    cookies.set(name, value, { ...option });
};

export const getCookie = (name: string) => {
    return cookies.get(name);
};

```

이런 식으로 쿠키를 setter 함수와 getter 함수를 생성하면 된다.


```ts
    const handleAddCookie = () => {
        setCookie('token', 'test');
    };


    const authTokenCookie = getCookie("accessToken");
    const refreshTokenCookie = getCookie("refreshToken")
```
