# CodeMirror 6 experiments

> **Historical experiments (2018–2019):** This repository explores early CodeMirror 6 packages in a Lerna workspace. It is not the current VZCode editor, and the original installation/watch instructions below are preserved for reference rather than guaranteed to run on current CodeMirror/Node versions.

## Repository layout and reproducibility

- [`packages/`](packages/) holds the experiment packages.
- The root [`package.json`](package.json) provides `npm run start` to bootstrap and run the legacy watch/start/test pipeline. This starts long-running development processes rather than performing a one-shot build.
- The historical `lerna` commands below may require earlier dependency versions and are **not verified** on current toolchains. Use a disposable local checkout, not a production environment.
- There is no root `npm test` script or current hosted service documented here.
- See [CodeMirror OT](https://github.com/vizhub-studio/codemirror-ot) and [VZCode](https://github.com/vizhub-studio/vzcode) for separate follow-on projects.

## Original experimental setup

Experiments with [CodeMirror 6](https://github.com/codemirror/codemirror.next). For background & writeup, see [Medium: Codemirror 6 Experiments](https://medium.com/@currankelleher/codemirror-6-experiments-a3930bf03781)

![image](https://user-images.githubusercontent.com/68416/47498132-f2be4b80-d879-11e8-8a02-8a66a36c6701.png)

To run:

```
git submodule update --init --recursive
npm install -g lerna
lerna bootstrap
lerna run build
lerna run start --stream
```
Then navigate to http://localhost:3000

To watch for changes and recompile automatically, run the following (in a separate terminal):

```
lerna run watch --stream
```
