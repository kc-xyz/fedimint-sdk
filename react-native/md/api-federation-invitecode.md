# FederationLike.inviteCode

```ts
inviteCode(): InviteCodeLike
```

Gives an invite `code` that you can share. Synchronous.

**Parameters.** None.

**Returns.** `InviteCodeLike`. An invite `code` for this `federation`.

**Throws.** None.

**Example**

`example.ts`

```ts
import type { FederationLike } from '@fedimint/react-native'

declare const fed: FederationLike

const invite = fed.inviteCode()
console.log(invite.federationId())
```

**Used in.** [Join, step 03](join.md#step-03)
