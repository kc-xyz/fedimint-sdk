# EcashQuoteLike.requestedAmount

```ts
requestedAmount(): Amount
```

Gives the amount that was asked for. Synchronous.

**Parameters.** None.

**Returns.** `Amount`. The amount that was asked for. It is a floor. It is not the amount the balance moves by.

**Throws.** None.

**Example**

`example.ts`

```ts
import type { EcashQuoteLike } from '@fedimint/react-native'

declare const quote: EcashQuoteLike

const msat = quote.requestedAmount()
console.log(`${msat / 1000n} sats`)
```

**Used in.** [Send, step 01](send.md#step-01)
