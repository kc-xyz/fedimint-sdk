# EcashSendOperationLike.requestCancel

```ts
requestCancel(): Promise<void>
```

Asks to take back the ecash of a send.

**Parameters.** None.

**Returns.** `Promise<void>`. Resolves when the cancel request is saved to storage. The outcome comes later, as the state `Canceled` or `Redeemed`. On a final state the call does nothing and does not fail.

**Throws.** [`Storage`](errors.md#code-storage), [`FederationClosed`](errors.md#code-federationclosed). This method never returns FederationUnreachable or Timeout.

**Example**

`example.ts`

```ts
import type { EcashSendOperationLike } from '@fedimint/react-native'

declare const operation: EcashSendOperationLike

await operation.requestCancel()
```

**Used in.** [Send, step 03](send.md#step-03)
