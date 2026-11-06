# EcashSendOperationLike.details

```ts
details(): Promise<EcashSendDetails>
```

Reads the details of an ecash send.

**Parameters.** None.

**Returns.** `EcashSendDetails`. The details of the send.

**Throws.** [`Storage`](errors.md#code-storage), [`FederationClosed`](errors.md#code-federationclosed), [`Internal`](errors.md#code-internal).

**Example**

`example.ts`

```ts
import type { EcashSendOperationLike } from '@fedimint/react-native'

declare const operation: EcashSendOperationLike

const details = await operation.details()
console.log(details.notes.display())
```

**Used in.** [History, step 04](history.md#step-04)
