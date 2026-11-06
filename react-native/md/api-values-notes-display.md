# NotesLike.display

```ts
display(): string
```

Gives the string to hand over. Synchronous.

**Parameters.** None.

**Returns.** `string`. The ecash string for the notes.

**Throws.** Not verified.

**Example**

`example.ts`

```ts
import type { NotesLike } from '@fedimint/react-native'

declare const notes: NotesLike

const text = notes.display()
console.log(text)
```

**Used in.** [Receive, step 01](receive.md#step-01), [Send, step 02](send.md#step-02), [History, step 04](history.md#step-04)
