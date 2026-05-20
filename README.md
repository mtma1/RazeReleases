# RAZE

**RAZE is a local-first AI workforce platform.**

RAZE lets you create AI employees, organize them into groups, assign jobs, and run an AI-powered workspace from your own machine. You bring your own model provider, your own API keys, and your own local runtime.

Website: [openraze.com](https://openraze.com)  
X: [@raze_devo](https://x.com/raze_devo)  
Creator: [@1mtma](https://x.com/1mtma)

---

## What is RAZE?

RAZE is built around a simple idea:

> AI should not only chat. It should work with structure, roles, context, approvals, and clear reports.

Instead of using one generic assistant for everything, RAZE gives you a local control center where you can create specialized AI employees, connect them to different models, group them together, and run tasks through a dashboard that you own.

RAZE is designed for builders, students, developers, creators, researchers, and teams who want AI workers that can help with real workflows while keeping control local.

---

## Key Features

### Local-first runtime

RAZE runs on your machine. The dashboard, runtime, employees, groups, jobs, and provider settings are managed locally.

### Bring your own model

Use your own provider and your own API keys. RAZE is designed to work with local models and API-based models.

Supported setup paths may include:

- OpenAI or OpenAI-compatible providers
- Ollama for local models
- Custom provider configuration

### AI employees

Create role-based AI workers such as:

- Researcher
- Developer
- Writer
- Product manager
- Tester
- Marketing assistant
- Custom employees for your own workflows

Each employee can have its own role, instructions, model, and behavior.

### Groups

Group multiple employees together so they can work as a team, discuss tasks, compare answers, and produce a final result.

### Jobs and tasks

Create manual or scheduled jobs and assign them to employees or groups.

### Local dashboard

RAZE includes a dashboard for managing:

- Employees
- Groups
- Jobs
- Provider settings
- Chat
- Runtime status
- Logs and reports

### Approval-first workflow

RAZE is designed around user control. Sensitive actions should be reviewed and approved by the user before execution.

---

## Quick Start

RAZE is installed through Python using `pip`.

### Requirements

- Python 3.11 or newer
- pip
- Windows, macOS, or Linux
- Optional: Ollama for local models
- Optional: API key for cloud model providers

---

## Install on Windows CMD

Use this in **Command Prompt**:

```cmd
python -m pip install --user --upgrade raze-cli
for /f "delims=" %i in ('python -c "import sysconfig; print(sysconfig.get_path('scripts'))"') do set "PATH=%PATH%;%i"
raze onboard
```

Then check RAZE status:

```cmd
raze status
```

The second line automatically adds the correct Python `Scripts` folder to the current terminal session. This helps when Windows says:

```txt
'raze' is not recognized as an internal or external command
```

Important: this PATH change is temporary for the current terminal window only.

---

## Install on PowerShell

Use this in **PowerShell**:

```powershell
python -m pip install --user --upgrade raze-cli
$env:PATH += ";" + (python -c "import sysconfig; print(sysconfig.get_path('scripts'))")
raze onboard
```

Then check RAZE status:

```powershell
raze status
```

---

## Install on macOS or Linux

```bash
python3 -m pip install --user --upgrade raze-cli
export PATH="$PATH:$(python3 -c 'import sysconfig; print(sysconfig.get_path("scripts"))')"
raze onboard
```

Then check RAZE status:

```bash
raze status
```

---

## First-Time Setup

Run:

```bash
raze onboard
```

This guides you through the first setup flow.

You can also run:

```bash
raze setup
```

Use setup to configure your model provider, local model, or API-based model.

To see the commands available in your installed version:

```bash
raze --help
```

---

## Common Commands

```bash
raze onboard
```

Run the first-time onboarding flow.

```bash
raze setup
```

Configure providers, models, and local settings.

```bash
raze status
```

Check the current RAZE runtime status.

```bash
raze doctor
```

Check your installation and runtime health.

```bash
raze update
```

Update the managed RAZE runtime bundle when a new version is available.

```bash
raze --help
```

Show all commands available in your installed version.

---

## How RAZE Works

RAZE is made of a few simple parts:

```txt
RAZE CLI
   |
   v
Local Runtime
   |
   +--> Core Service
   |
   +--> Local Dashboard
   |
   +--> Employees
   |
   +--> Groups
   |
   +--> Jobs
   |
   +--> Provider Settings
```

The CLI starts and manages the local runtime through onboarding and runtime commands.  
The dashboard gives you a visual control center.  
The core service coordinates employees, jobs, providers, and local state.

---

## Core Concepts

### Employee

An employee is an AI worker with a role.

Example:

```txt
Name: Code Reviewer
Role: Reviews code, finds bugs, suggests safer changes.
Model: OpenAI / Ollama / Custom provider
```

### Group

A group is a team of employees.

Example:

```txt
Group: Product Launch Team
Employees:
- Researcher
- Copywriter
- Designer
- QA Tester
```

### Job

A job is a task assigned to an employee or group.

Example:

```txt
Task: Review the landing page copy and suggest improvements.
Assignee: Marketing Group
Schedule: Manual
```

### Provider

A provider is the model source RAZE uses.

Examples:

```txt
OpenAI
Ollama
Custom OpenAI-compatible API
```

---

## Local-First Philosophy

RAZE is local-first by design.

That means:

- The runtime runs on your machine.
- Your dashboard is served locally.
- Your provider settings are owned by you.
- You decide which model to use.
- You decide which actions to approve.

Important note:

Local-first does not mean every model runs offline. If you use an API provider, your prompts and responses may be sent to that provider according to their terms. If you use a local model through Ollama, the model can run on your own device.

---

## Security and Responsibility

RAZE is a powerful local AI platform. You are responsible for how you configure it and what you allow it to do.

Recommended safety rules:

- Do not paste secrets into public chats.
- Review actions before approving them.
- Use local models when privacy is critical.
- Use API providers only when you understand their data policies.
- Keep your API keys private.
- Do not give broad access to tools unless you trust the task and the model.

RAZE is designed to make AI work more useful, but final responsibility stays with the user.

---

## Troubleshooting

### `raze` command is not recognized on Windows

Run this in CMD:

```cmd
for /f "delims=" %i in ('python -c "import sysconfig; print(sysconfig.get_path('scripts'))"') do set "PATH=%PATH%;%i"
```

Then run:

```cmd
raze onboard
```

If it still does not work, close the terminal, open it again, and try:

```cmd
python -m pip install --user --upgrade raze-cli
```

Then repeat the PATH command above.

---

### Check if RAZE is installed

```bash
python -m pip show raze-cli
```

---

### Upgrade RAZE CLI

```bash
python -m pip install --user --upgrade raze-cli
```

---

### Check installation health

```bash
raze doctor
```

---

### Check runtime status

```bash
raze status
```

---

## Example Use Cases

RAZE can help with workflows like:

- Code review
- Research
- Content planning
- Project management
- Testing plans
- Documentation writing
- Marketing drafts
- Local AI experiments
- Multi-agent brainstorming
- Personal productivity workflows

---

## Project Status

RAZE is under active development.

The platform is evolving quickly, and some features may change as the product improves.

Current focus areas:

- Better onboarding
- Easier provider and model setup
- Stronger local runtime reliability
- Better dashboard user experience
- More useful employees and groups
- Safer approval workflows
- Clearer logs, reports, and task results
- Arabic and English experience

---

## Arabic Summary

**ريز RAZE** هي منصة ذكاء اصطناعي محلية أولًا، تسمح لك بإنشاء موظفين ذكاء اصطناعي، تنظيمهم داخل مجموعات، وتشغيل المهام من لوحة تحكم محلية على جهازك.

الفكرة الأساسية:

> بدل ما يكون عندك مساعد واحد فقط، RAZE يعطيك فريق من موظفي الذكاء الاصطناعي، كل واحد له دور، نموذج، وتعليمات خاصة.

RAZE مناسب للمطورين، الطلاب، صناع المحتوى، الباحثين، وأي شخص يريد استخدام الذكاء الاصطناعي بطريقة منظمة وقابلة للإدارة.

### أهم فكرة

RAZE لا يحاول يأخذ التحكم منك.  
أنت تختار النموذج، المزود، المفاتيح، والمهام التي توافق على تنفيذها.

---

## Arabic Quick Start

على Windows CMD:

```cmd
python -m pip install --user --upgrade raze-cli
for /f "delims=" %i in ('python -c "import sysconfig; print(sysconfig.get_path('scripts'))"') do set "PATH=%PATH%;%i"
raze onboard
```

ثم تحقق من الحالة:

```cmd
raze status
```

إذا ظهر لك أن أمر `raze` غير معروف، فهذا غالبًا بسبب أن مسار Python Scripts غير مضاف للـ PATH. الأمر الثاني في الأعلى يحل المشكلة مؤقتًا داخل نفس نافذة التيرمنل.

---

## License

RAZE is released under the MIT License.

See the `LICENSE` file for details.

---

## Links

Website: [openraze.com](https://openraze.com)  
X: [@raze_devo](https://x.com/raze_devo)  
Creator: [@1mtma](https://x.com/1mtma)
