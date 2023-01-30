1. check out the first commit

`$ npm install`  
`$ npm run example`

observe no error

2. check out the second commit

`$ npm install`  
`$ npm run example`

See this error:

```
repro-svelte-component-not-assignable/src/App.svelte:5:2
Error: Argument of type 'typeof OtherComponent__SvelteComponent_' is not assignable to parameter of type 'ConstructorOfATypedSvelteComponent'.
  Type 'OtherComponent__SvelteComponent_' is missing the following properties from type 'ATypedSvelteComponent': $$prop_def, $$events_def, $$slot_def, $on

Possible causes:
- You use the instance type of a component where you should use the constructor type
- Type definitions are missing for this Svelte Component. If you are using Svelte 3.31+, use SvelteComponentTyped to add a definition:
  import type { SvelteComponentTyped } from "svelte";
  class ComponentName extends SvelteComponentTyped<{propertyName: string;}> {} (ts)

<OtherComponent />
```
