# Free credits Setup Guide

## Step 1: Get Your API Key

1. Go to the [Agent Router Portal](https://agentrouter.org/register?aff=fpCu) (interface may load in Chinese — switch to English via the browser translate option).
2. Sign in with your any GitHub account.
3. Create an account and navigate to the **Dashboard** tab. (you will see 175$ credits in wallet)
4. Go to **API Token** in the left menu and click **Create Token**.
5. Configure the token permissions, enable the "Unlimited quota" option, and copy your API key (starts with `sk-`).

## Step 2: Install Claude Code

Choose one of the following:
- Install the **Claude Code extension** from the VS Code Marketplace, or
- Install via terminal / the official Claude Code installation method.

## Step 3: Configure `settings.json`

**File location:**
- **Linux/macOS:** `~/.claude/settings.json`
- **Windows:** `%USERPROFILE%\.claude\settings.json`

Open the file and replace its contents with:
```json
​{
  "env": {
    "ANTHROPIC_API_KEY": "Your_token",
    "ANTHROPIC_BASE_URL": "https://agentrouter.org",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": "1",
    "MAX_THINKING_TOKENS": "30000",
    "CLAUDE_CODE_AUTO_COMPACT_WINDOW": "1000000",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "glm-5.3[1m]",
    "ANTHROPIC_DEFAULT_FABLE_MODEL": "gpt-5.6-sol[1m]",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "claude-opus-5[1m]",
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "claude-opus-4-8[1m]"
  },
  "model": "opus",
  "enableWorkflows": true,
  "effortLevel": "high",
  "theme": "dark",
  "autoCompactEnabled": false,
  "claudeCode.disableLoginPrompt": true,
  "claudeCode.initialPermissionMode": "acceptEdits"
}


```

> **Important:** Replace `YOUR_TOKEN` with your actual key from Step 1.

**Supported models and thier model IDs:**  (you can replace this with your model in setting.json)

- claude-opus-4-8[1m]
- claude-opus-5[1m]
- gpt-5.6-sol
- glm-5.3

>[!CAUTION]
>**Note:**  Claude and GPT models will be available on a *limited daily quota*, distributed in batches throughout the day. Once a batch is used up, it will not be available until the next batch is released.
>
>If the current batch is exhausted, Claude / GPT will be temporarily unavailable. The error message is displayed as"402 Budget pool quota has been exhausted." — simply wait for the next batch. Alternatively, you can switch to *DeepSeek / GLM models* and continue using them as usual.

## Step 4: Start the Claude

Open a **new terminal window** so the settings take effect, then run:

```bash
claude
```

If prompted to confirm the custom `ANTHROPIC_API_KEY`, type `y` to accept.
Run `/status` to confirm your setup is active.

## Key Points: 
1. You can use Codex, Cursor and anyother platform also. Here's official [Setup guide](https://agentrouter.org/docs/claude-code.html).
2. Use the agentrouter which is present in this guide. as you will get 50$ extra otherwise you will get only 125$.
3. Sometimes Claude code will give "Api 400 error". To resolve that there are few troubleshoots: (Chinese maal h bhai, m bhi iska kuch nhi kar sakta hu)
   - Command 'continue' to keep your work ongoing.
   - If you still see error, then In setting.json, Set `"MAX_THINKING_TOKENS"` to 0.
   - If still error remains, then use cursor or codex rather than claude code


## Enjoy...
