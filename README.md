# zipfs-bug minimal repro

- Open this workspace with Typescript 1.48
- Open `index.ts`
- Jump to the definition of `L` in `console.log(L)`

This will fail with a message like this:

> Unable to open 'index.d.ts': Unable to read file '/zip:/Users/me/src/project/.yarn/cache/@types-leaflet-npm-1.5.17-401fcefaf4-a596fb8672.zip/node\_modules/@types/leaflet/index.d.ts' (Error: Unable to resolve non-existing file '/zip:/Users/me/src/project/.yarn/cache/@types-leaflet-npm-1.5.17-401fcefaf4-a596fb8672.zip/node\_modules/@types/leaflet/index.d.ts').

- Open this workspace with Typescript 1.47
- Open `index.ts`
- Jump to the definition of `L` in `console.log(L)`

This will open `index.d.ts` in `@types/leaflet`.
