# commitlint-config-viki

Viki's shareable [commitlint](https://github.com/conventional-changelog/commitlint) config.

## Usage

Install `commitlint-config-viki`

```bash
npm i -D commitlint commitlint-config-viki    # npm
pnpm add -D commitlint commitlint-config-viki # pnpm
```

Configurate your `commitlint.config.js`

```js
module.exports = {
  extends: ['viki'],
};
```

## Work with `cz-customizable`

If you use `cz-customizable`, install `commitlint-config-cz`.

[`commitlint-config-cz`](https://github.com/whizark/commitlint-config-cz) will automatically merge your config in `.cz-config.json` and `commitlint.config.js`.

```bash
npm i -D commitlint-config-cz     # npm
pnpm add -D commitlint-config-cz  # pnpm
```

```js
module.exports = {
  // add 'cz' at the end of extends array
  extends: ['viki', 'cz'],
};
```

## Work with `husky`

Husky improves your commits and more 🐶 woof!

```bash
# init husky with initialization script && install husky
npx husky-init && npm install       # npm
pnpm dlx husky-init && pnpm install # pnpm
```

```bash
# add commit-msg hook
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'
```
