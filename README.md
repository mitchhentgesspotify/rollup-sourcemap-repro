1. `cd lib`
   1. `npm i`
   2. `./node_modules/.bin/rollup -c`
   3. `npm pack`
2. `cd consumer`
   1. `npm i ../lib/lib-0.0.1.tgz`
3. Open the *`consumer` subdirectory* in IntelliJ
4. Put a breakpoint on line 2 of `main.js`
5. Run `main.js` and debug it
6. When it stops on line 2, click to "step in"
7. It'll bring you to a virtual `lib.ts` file. Try to put a breakpoint anywhere in the file. It won't work.

If you look at `Help > Show Log in Finder > idea.log`, you'll see something like:

```
2024-04-02 15:17:55,753 [10406363]   WARN - #c.i.j.d.JavaScriptDebugProcess - Unable to set breakpoint with null position: mock://file:///Users/mhentges/dev/rollup-sourcemap-repro/consumer/node_modules/lib/lib.js
```
