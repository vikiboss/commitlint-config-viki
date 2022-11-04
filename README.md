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

## Work with `commitizen`

Generate `commitizen` config using `commitlint` config.

Install `@commitlint/cz-commitlint`.

```bash
npm i -D @commitlint/cz-commitlint     # npm
pnpm add -D @commitlint/cz-commitlint  # pnpm
```

Configurate your `package.json`:

```json
{
  "config": {
    "commitizen": {
      "path": "node_modules/@commitlint/cz-commitlint"
    }
  }
}
```

Then you can use `git cz` for `commitizen` commit.

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
