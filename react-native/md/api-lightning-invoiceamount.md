# LnQuoteLike.invoiceAmount

```ts
invoiceAmount(): Amount
```

Gives the amount of the invoice. Synchronous.

**Parameters.** None.

**Returns.** `Amount`. What reaches the payee.

**Throws.** None.

**Example**

`example.ts`

```ts
import type { LnQuoteLike } from '@fedimint/react-native'

declare const quote: LnQuoteLike

const msat = quote.invoiceAmount()
console.log(`${msat / 1000n} sats`)
```

**Used in.** [Send, step 04](send.md#step-04)
