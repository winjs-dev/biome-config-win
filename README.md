# @winner-fed/biome-config-win

团队的 Biome 共享配置，提供统一的代码格式化和检查规则。

## 安装

```bash
npm install --save-dev @winner-fed/biome-config-win @biomejs/biome
```

或使用 pnpm:

```bash
pnpm add -D @winner-fed/biome-config-win @biomejs/biome
```

## 使用方法

在你的项目根目录创建 `biome.json` 文件并引用此配置：

```json
{
  "$schema": "https://biomejs.dev/schemas/2.0.0/schema.json",
  "extends": ["@winner-fed/biome-config-win"]
}
```

## 配置说明

### 格式化规则

- **缩进**: 2 个空格
- **行宽**: 120 字符
- **换行符**: LF
- **JavaScript**:
  - 单引号
  - JSX 使用双引号
  - 始终使用分号
  - 箭头函数参数始终使用括号
  - 不使用尾随逗号
- **JSON**: 不使用尾随逗号
- **CSS/LESS**: 双引号

### Linter

启用所有推荐规则。

### 版本控制

- 集成 Git
- 自动使用 `.gitignore` 文件

## 在 package.json 中添加脚本

```json
{
  "scripts": {
    "format": "biome format --write .",
    "lint": "biome lint .",
    "check": "biome check --write ."
  }
}
```

## License

MIT © winjs-dev
