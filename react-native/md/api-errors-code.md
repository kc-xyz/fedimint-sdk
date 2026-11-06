# ExceptionLike.code

```ts
code(): ErrorCode
```

Gives the stable error `code`. Synchronous.

**Parameters.** None.

**Returns.** `ErrorCode`. The stable `code`. Branch on it.

**Throws.** None.

**Example**

`example.ts`

```ts
import { ErrorCode, type ExceptionLike } from '@fedimint/react-native'

declare const inner: ExceptionLike

const code = inner.code()
console.log(ErrorCode[code])
```

**Used in.** [Errors, step 01](errors.md#step-01)
