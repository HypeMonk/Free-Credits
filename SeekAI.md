# Free credits Setup Guide (SeekAI)

## Step 1: Get Your API Key

1. Go to the [SeekAI Portal](https://seekai.cc/sign-up?aff=fQ56) (Signup with this link.. you will get some bonus)
2. Sign in with your any GitHub account. (must be older than 1 year)
3. Create an account and navigate to the **Dashboard** tab. (you will upto 200$ credits in wallet)
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
    "ANTHROPIC_BASE_URL": "https://seekai.cc",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": "1",
    "MAX_THINKING_TOKENS": "30000",
    "CLAUDE_CODE_AUTO_COMPACT_WINDOW": "1000000",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "claude-sonnet-5[1m]",
    "ANTHROPIC_DEFAULT_FABLE_MODEL": "claude-fable-5[1m]",
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

**Supported models and thier model IDs:**  (you will get all options in /model)

- claude-fable-5[1m]
- claude-opus-5[1m]
- claude-opus-4-8[1m]
- claude-sonnet-5[1m]
- and many more models (https://seekai.cc/pricing)


## Step 4: Start the Claude

Open a **new terminal window** so the settings take effect, then run:

```bash
claude
```

If prompted to confirm the custom `ANTHROPIC_API_KEY`, type `y` to accept.
Run `/status` to confirm your setup is active.



## Enjoy...
