# MnemonicLike.words

```ts
words(): Array<string>
```

Reads the seed `words`. Synchronous.

**Parameters.** None.

**Returns.** `Array<string>`. The seed `words`, in order. This call is the deliberate act of taking the seed out of the SDK.

**Throws.** None.

**Example**

`example.ts`

```ts
import type { MnemonicLike } from '@fedimint/react-native'

declare const mnemonic: MnemonicLike

const words = mnemonic.words()
console.log(words.length)
```

**Used in.** [Seed words, step 02](seed-words.md#step-02), [Restore, step 02](restore.md#step-02), [Installation, step 06](installation.md#step-06)
