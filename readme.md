# react-page-fitter

[![Release Status](https://img.shields.io/github/release/su-pull/react-page-fitter.svg)](https://github.com/su-pull/react-page-fitter/releases/latest)
![code size](https://img.shields.io/github/languages/code-size/su-pull/react-page-fitter)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This is a React hooks that observe HTML element fits within the current viewport.

## Installation

```sh
npm install react-page-fitter
```

## Usage

```tsx
import useFitter, { Main } from 'react-page-fitter'

function MyComponent({ children }) {
  const { pathname } = useLocation()
  const isFit = useFitter()

  return (
    <>
      {isFit !== undefined && (
        <Main location={pathname} classFitIn={style} classFitOut={style}>
          {children}
        </Main>
      )}
    </>
  )
}
```

## API

useFitter (ref, pathname, {options})  
return value is boolean or undefined.

## Parameters

- ref (optional): RefObject to the HTML element to be observe.  
  If not set, it will observe the imported component.

- pathname (optional): Set a current dynamic pathname.  
  This is the function trigger.

- options (optional): viewport property values.

  1\. offsetX: A number representing the horizontal offset to use if the element fits.  
  The default value is 0.

  2\. offsetY: A number representing the vertical offset to use if the element fits.  
  The default value is 0.

## License

The MIT License.
