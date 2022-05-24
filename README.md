# create-react-app 创建工程

### npx create-react-app jira --template typescript

# prettier 统一格式化工程文件

### yarn add --dev --exact prettier

### echo {}> .prettierrc.json

# 创建一个.prettierignore 文件 Ignore artifacts:

build
coverage

#手动使用 prettier 格式化所有文件

### yarn prettier --write .

# 检查文件是否符合 prettier 规范

### npx prettier --check .

# Install eslint-config-prettier:

### npm install --save-dev eslint-config-prettier

# 添加 "prettier" 到 "extends"中最后面

{
"extends": [
"some-other-config-you-use",
"prettier"
]
}

# Install husky and lint-staged:

### yarn add --dev husky lint-staged

### npx husky install

### npm set-script prepare "husky install"

### npx husky add .husky/pre-commit "npx lint-staged"

# Add the following to your package.json:

{
"lint-staged": {
"\*_/_": "prettier --write --ignore-unknown"
}
}

# 规范 git commit message

### npm install --save-dev @commitlint/config-conventional @commitlint/cli

### echo "module.exports = {extends: ['@commitlint/config-conventional']};" > commitlint.config.js

# 提交方法：

[
'build',
'chore',
'ci',
'docs',
'feat',
'fix',
'perf',
'refactor',
'revert',
'style',
'test'
];

### echo "foo: some message" # fails

### echo "fix: some message" # passes

### npx husky add .husky/commit-msg "npx yarn commitlint --edit $1"

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
