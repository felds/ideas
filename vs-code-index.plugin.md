# VSCode index plugin

On the tree view, it should put a marker (like a `*`) on folders with index
files. Clicking the folder, it would open the index in the editor.

It should show only the folder name on the tab bar.

In the tree:
```txt
├── filter *
├── footer *
│   ├── footer.module.css
│   ├── logo.svg
├── header
│   ├── not-an-index.tsx
│   ├── header.module.css
```

In the tab bar:

```txt
|  footer *  |  footer.module.css  |  not-an-index.tsx  |
```


## Why?

* Ryan Dahl — the creator of NodeJS — [regrets][1] having `index.js` as a default
    module's file. Why not fixing it on the editor?

* When using css modules in React et al, every folder ends up getting an 
    `index.tsx` file (either for pointing to a named file component or for the
    component itself). It makes the tree looks larger than needed and adds a lot
    of noise.

* Having a lot of tabs named `index.tsx` is not very informative and does not
    convey the meaning of being a module named `foo`, not a regular file named
    `foo/index.tsx`.


## Known Unknowns

* Is the `*` symbol ideal for denoting indices?

* What if there are multiple indices in a folder (eg: `dist/index.cjs`, 
    `dist/index.d.ts`, `dist.mjs`)

* How to deal with the open file palette? 




<!--  -->

[1]: https://www.youtube.com/watch?v=M3BM9TB-8yA&t=835s