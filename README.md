# apifoxmcp

Apifox 场景用例的 stdio MCP。令牌放在本地 `config.yaml`，不要提交。

```yaml
api_fox_tokens: <个人访问令牌>
```

Cursor 里启动：

```json
{
  "mcpServers": {
    "apifox": {
      "command": "python3",
      "args": ["server.py"]
    }
  }
}
```

个人令牌不能直接在 `main` 上新建场景。先 `create_automation_branch`，需要的接口用 `pick_endpoints` 挑进该分支，再用 `create_scenario` / `update_scenario` 写步骤。
