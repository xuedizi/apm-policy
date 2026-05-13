# apm-policy

组织级 APM 治理基线。所有引用 `xuedizi/apm-policy#vX.Y.Z` 的 `apm-policy.yml`
在 `extends:` 时继承这里的策略。子策略遵循 `tighten_only`,只能继续收紧,不能放开。

## 引用方式

```yaml
# 子项目 apm-policy.yml
extends: xuedizi/apm-policy#v1.0.0
```

## 内容

| 文件 | 说明 |
|---|---|
| `policy.yml` | ★ 基线;`extends: xuedizi/apm-policy#v1.0.0`(无 path)解析到此 |
| `CHANGELOG.md` | 版本变更记录 |
| `VERSION` | 单一版本事实源,CI 校验与 tag 一致 |
| `examples/` | 合法子策略参考(可直接 copy 修改) |

## 版本节奏

| 变更类型 | bump | 说明 |
|---|---|---|
| 新增 `denied` / 缩窄 `allowed_*` | **major** | 影响所有下游,需明告 |
| 放开 `denied` / 扩宽 `allowed_*` | minor | 兼容性增强 |
| 注释 / metadata | patch | 仅文档 |

## License

[MIT](LICENSE)
