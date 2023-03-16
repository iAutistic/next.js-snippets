# Nextjs Snippets

Latest snippets for nextjs

![next js-snippets-gif](https://user-images.githubusercontent.com/50038851/85401251-59c46400-b577-11ea-9eb3-a8ed916c711e.gif)

## Installation

- install the extension
- reload vscode
- snippets will be ready to use



# New Snippets

### `nspage` (nextjs page with getServerSideProps)

#### Javascript

```js
export default function Test() {
  return <div>Enter</div>;
}

export async function getServerSideProps(ctx) {
  return {
    props: {
      data: null,
    },
  };
}
```

#### Typescript

```ts
import { GetServerSideProps } from "next";

const Test = () => {
  return <div>Enter</div>;
};

export const getServerSideProps: GetServerSideProps = async (ctx) => {
  return {
    props: {},
  };
};

export default Test;
```

### `nstaticpage` (nextjs page with getStaticProps and getStaticPaths)

#### Javascript

```js
export default function Test() {
  return <div>Enter</div>;
}

export async function getStaticPaths() {
  return {
    paths: [],
    fallback: false,
  };
}
export async function getStaticProps(ctx) {
  return {
    props: {
      data: null,
    },
  };
}
```

#### Typescript

```ts
import { GetStaticPaths, GetStaticProps } from "next";

const test = () => {
  return <div>Enter</div>;
};

export const getStaticPaths: GetStaticPaths = () => {
  return {
    paths: [],
    fallback: false,
  };
};
export const getStaticProps: GetStaticProps = async (ctx) => {
  return {
    props: {},
  };
};

export default test;
```

### `nnotfound` (nextjs not found page)

#### Javascript

```js
export default function test() {
    return (
        <div>
            <h1>
                Page Not Found
            </h1>
        </div>
    );
}
```

### `nservererror` (nextjs server error page)

#### Javascript

```js
export default function test() {
    return (
        <div>
            <h1>
                Server Error
            </h1>
        </div>
    );
}
```

### `ngetServerSideProps` (nextjs getServerSideProps function)

#### Javascript

```js
export async function getServerSideProps(ctx){


    return {
        props:{
            data:null
        }
    }
}
```

#### Typescript

```ts
export const getServerSideProps: GetServerSideProps = async (ctx) => {


    return {
        props:{

        }
    }
}
```

### `ngetStaticProps` (nextjs getStaticProps function)

#### Javascript

```js
export async function getStaticProps(ctx) {


    return {
        props:{
            data:null
        }
    }
}
```

#### Typescript

```ts
export const getStaticProps: GetStaticProps = (ctx) => {


    return {
        props:{

        }
    }
}
```

### `ngetStaticPaths` (nextjs getStaticPaths function)

#### Javascript

```js
export async function getStaticPaths() {


    return {
        paths:[],
        fallback:false
    }
}
```

#### Typescript

```ts
export const getStaticPaths: GetStaticPaths = () => {


    return {
        paths:[],
        fallback:false
    }
}
```

### `nul` (nextjs use link element)

#### Javascript

```js
<Link href='path'>link</Link>
```



# Javascript

## Page initialization snippets

### `nafe` (nextjs arrow function (export at the end))

```js
const FileName = () => {
  return <div>CONTENT</div>;
};

export default FileName;
```

### `naf` (nextjs arrow function)

```js
export default () => {
  return <div>CONTENT</div>;
};
```

### `nfe` (nextjs normal function (export at the end))

```js
function FileName() {
  return <div>CONTENT</div>;
}

export default FileName;
```

### `nf` (nextjs normal function )

```js
export default function () {
  return <div>CONTENT</div>;
}
```

## Nextjs snippets

### `ngsspr` (nextjs getServerSideProps)

#### Javascript 
```js
export const getServerSideProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};
```

#### Typescript
```ts
export const getServerSideProps: GetServerSideProps = async (ctx) => {
    return {
        props:{
            data:null
        }
    }
}
```

### `ngspr` (nextjs getStaticProps)

#### Javascript

```js
export const getStaticProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};
```

#### Typescript

```ts
export const getStaticProps: GetStaticProps = async (ctx) => {
    return {
        props:{
            data:null
        }
    }
}
```

### `ngspa` (nextjs getStaticPaths)

#### Javascript

```js
export const getStaticPaths = async () => {
  return {
    paths: [],
    fallback: false,
  };
};
```

#### Typescript

```ts
export const getStaticPaths: GetStaticPaths = async () => {
    return {
        paths:[],
        fallback:false
    }
}
```

### `ngipr` (nextjs getInitialProps)

```js
FileName.getInitialProps = async (ctx) => {

    return {
        ${3:data:null}
    }
}
```

## Nextjs Custom app and document (\_app.js,\_document.js)

### `ncapp` (nextjs custom app)

#### Javascript

```js
export default function MyApp({ Component, pageProps }) {
    return <Component {...pageProps} />
}
```

#### Typescript

```ts
import type {AppProps} from 'next/app'

const MyApp = ({ Component, pageProps }:AppProps) => {
    return <Component {...pageProps} />
}

export default MyApp;
```

### `ncdocument` (nextjs custom document)

#### Javascript

```js
import { Html, Head, Main, NextScript } from 'next/document'

export default function Document() {
    return (
        <Html>
            <Head/>
            <body>
                <Main />
                <NextScript />
            </body>
        </Html>
    )
}
```


## Nextjs api routes

### `napi` (nextjs api route)

#### Javascript

```js
export default function handler(req, res)  {
    req.statusCode = 200
}
```

#### Typescript

```ts
import { NextApiRequest, NextApiResponse } from 'next';

export default function handler(req:NextApiRequest, res:NextApiResponse) {
    req.statusCode = 200
}
```

## Nextjs page initialization function with Nextjs functions

### `nafewserver` (nextjs arrow function (export at the end) with getServerSideProps)

#### Javascript

```js
const FileName = () => {
  return <div>CONTENT</div>;
};

export const getServerSideProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};

export default FileName;
```

#### Typescript

```ts
import { GetServerSideProps } from 'next';

const Test = () => {
    return (
        <div>
            Enter
        </div>
    );
}

export const getServerSideProps:GetServerSideProps = async (ctx) => {
    return {
        props:{
            data:null
        }
    }
}

export default Test;
```

### `nfewserver` (nextjs normal function (export at the end) with getServerSideProps)

#### Javascript 

```js
function FileName() {
  return <div>CONTENT</div>;
}

export async function getServerSideProps(ctx) {
  return {
    props: {
      data: null,
    },
  };
}

export default FileName;
```

### `nafewstatic` (nextjs arrow function (export at the end) with getStaticProps)

#### Javascript

```js
const FileName = () => {
  return <div>CONTENT</div>;
};

export const getStaticProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};

export default FileName;
```

#### Typescript

```ts
import {GetStaticProps} from 'next';

const Test = () => {
    return (
        <div>
            Enter
        </div>
    );
}

export const getStaticProps:GetStaticProps = async (ctx) => {


    return {
        props:{
            data:null
        }
    }
}

export default Test;
```

### `nfewstatic` (nextjs normal function (export at the end) with getStaticProps)

#### Javascript

```js
function FileName() {
  return <div>CONTENT</div>;
}

export async function getStaticProps(ctx) {
  return {
    props: {
      data: null,
    },
  };
}

export default FileName;
```

## Static generation snippet

### `!!static` (initializing function with getStaticPaths and getStaticProps)

#### Javascript

```js
const FileName = () => {
  return <div>CONTENT</div>;
};

export const getStaticPaths = async () => {
  return {
    paths: [],
    fallback: false,
  };
};

export const getStaticProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};

export default FileName;
```

#### Typescript

```ts
import {GetStaticPaths,GetStaticProps} from 'next';

const Test = () => {
    return (
        <div>
            Enter
        </div>
    );
}

export const getStaticPaths:GetStaticPaths = async () => {
    return {
        paths:[],
        fallback:false
    }
}
export const getStaticProps:GetStaticProps = async (ctx) => {
    return {
        props:{
            data:null
        }
    }
}

export default Test;
```

## Importing Components

### `nil` (nextjs import link)

```js
import Link from "next/link";
```

### `nir` (nextjs import router(default))

```js
import Router from "next/router";
```

### `niur` (nextjs import useRouter)

```js
import { useRouter } from "next/router";
```

### `nih` (nextjs import Head)

```js
import Head from "next/head";
```

## Imported Components Usage

### `nulwhref` (nextjs use link with href)

```js
<Link href="path">
  <a>Value</a>
</Link>
```

### `nuur` (nextjs use useRouter)

```js
const router = useRouter();
```

### `nuh` (nextjs use Head )

```js
<Head>
  <title>Title</title>
</Head>
```

### `nul` (nextjs use Image component)

```js
<Image src='path' width='width' height='height' alt='alt' />
```


## Deprecated Typescript Snippets

## Nextjs page initialization function with Nextjs functions

### `ntsfwserver` (nextjs typescript function with getServerSideProps (DEPRECATED))

```ts
import { GetServerSideProps } from "next";

const FileName = () => {
  return <div>CONTENT</div>;
};

export const getServerSideProps: GetServerSideProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};

export default FileName;
```

### `ntsfwstatic` (nextjs typescript function with getStaticProps (DEPRECATED))

```ts
import { GetStaticProps } from "next";

const FileName = () => {
  return <div>CONTENT</div>;
};

export const getStaticProps: GetStaticProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};

export default FileName;
```

## Nextjs api routes

### `ntsapi` (nextjs typescript api route (DEPRECATED))

```ts
import { NextApiRequest, NextApiResponse } from "next";

export default (req: NextApiRequest, res: NextApiResponse) => {};
```

## Nextjs Custom app and document (\_app.js,\_document.js)

### `ntscapp` (nextjs typescript custom app)

```ts
import { AppProps } from 'next/app';

const MyApp = ({ Component pageProps }:AppProps) => {
    return <Component {...pageProps} />
}

export default MyApp;
```

### `ntscdocument` (nextjs typescript custom document (DEPRECATED))

```js
import Document, { Html, Head, Main, NextScript } from "next/document";

class MyDocument extends Document {
  static async getInitialProps(ctx) {
    const initialProps = await Document.getInitialProps(ctx);
    return { ...initialProps };
  }

  render() {
    return (
      <Html>
        <Head />
        <body>
          <Main />
          <NextScript />
        </body>
      </Html>
    );
  }
}

export default MyDocument;
```

## Static generation snippet

### `!!tsstatic` (initializing function with getStaticPaths and getStaticProps(typescript) (DEPRECATED))

```ts
import { GetStaticPaths, GetStaticProps } from "next";
const FileName = () => {
  return <div>CONTENT</div>;
};

export const getStaticPaths: GetStaticPaths = async () => {
  return {
    paths: [],
    fallback: false,
  };
};

export const getStaticProps: GetStaticProps = async (ctx) => {
  return {
    props: {
      data: null,
    },
  };
};

export default FileName;
```
