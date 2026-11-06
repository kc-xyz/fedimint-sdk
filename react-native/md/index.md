# Add ecash and Lightning to the app you already have

Join a federation, hold ecash, send and receive it, and restore from seed words, with one typed SDK.

```sh
npm install --save-exact @fedimint/react-native@0.1.0-beta.4 @fedimint/react-native-bindings@0.1.0-beta.4
cd ios && pod install
```

```tsx
const session = await openSdk({ dataDir })
const fed = await session.sdk.join(InviteCode.parse(code))
const msat = useBalance(fed)
return <Text>{`${msat / 1000n} sats`}</Text>
```

## What is Fedimint

[Fedimint](https://fedimint.org) is an open source protocol that lets a group of guardians, a _federation_, hold bitcoin together for a community. The federation issues **ecash**: digital notes, backed by that bitcoin, that your wallet keeps on the device. Ecash payments are fast, cheap and private, and a Lightning gateway connects them to the Lightning Network.

In short: your app holds ecash and talks to one federation. The federation reaches Lightning through a gateway. Your app can also give notes straight to another wallet.

## What this SDK does

This guide follows one path, from an empty project to a wallet that joins a federation, holds ecash, moves it two ways, lists its history and restores itself from seed words. It uses two npm packages. You import everything from `@fedimint/react-native`. It adds `openSdk` and two React hooks, `useBalance` and `useOperation`. `@fedimint/react-native-bindings` holds the native part, generated from the Rust crate `rust/fedimint-sdk`. Your app lists both.

The packages ship prebuilt native libraries for iOS 15.0 or newer and Android API 24 or newer. Nothing compiles when you install them. They need the New Architecture, and they do not run in Expo Go. Expo apps use a config plugin and a development build.

Amounts are millisatoshis (msat), as a `bigint`. A failed payment is a state that you observe, not an error that is thrown. Every code block in this guide is compiled against the packages before it is published here.

This guide does not cover on chain send and receive. A federation that supports them gives you `fed.onchain()`.

## Where to start

- [**Quickstart**](quickstart.md): From an empty app to a balance on screen in one page.
- [**Guides**](join.md): One task each: join, balance, receive, send, history, share the session, restore.
- [**Reference**](errors.md): Errors, amounts, and seed words.

## For AI agents

An agent can follow this guide from start to end. Every page is also plain Markdown. Give the agent one of these files:

- [**llms-full.txt**](/react-native/llms-full.txt): Every page in one file. Use this one first.
- [**llms.txt**](/react-native/llms.txt): The list of pages, with a link to each page as Markdown.
- <a href="/react-native/md/quickstart.md" target="_blank"><strong>md/quickstart.md</strong></a>: One page as plain Markdown. Every page has one, at `md/<page>.md`.
- [**SKILL.md**](https://github.com/fedimint/fedimint-sdk/blob/main/skills/fedimint-react-native-install/SKILL.md): An agent skill for a first install in an existing app: checks, safety rules, failures and a definition of done.

Then give the agent this prompt:

```text
Read llms-full.txt from the Fedimint SDK for React Native guide.
Add the SDK to this React Native app. Follow the pages in order,
from Installation to Restore from seed words. Install the exact
package versions that the guide gives. Make sure that each step
works before you start the next one.
```

## The pages

- [Quickstart](quickstart.md)
- [Installation](installation.md)
- [Join a federation](join.md)
- [Show a balance](balance.md)
- [Receive money](receive.md)
- [Send money](send.md)
- [See the history](history.md)
- [Share the session](session.md)
- [Restore from seed words](restore.md)
- [Errors](errors.md)
- [Amounts](amounts.md)
- [Seed words](seed-words.md)
