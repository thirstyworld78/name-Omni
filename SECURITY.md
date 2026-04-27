# Security Policy

## Reporting a Vulnerability

If you discover a vulnerability, misuse scenario, or potential safety bypass in the Omni agent configuration, we want to hear from you. This includes:

- Prompt injection or manipulation that could bypass ethical guardrails.
- Unintended behavior leading to unauthorized scanning or destructive actions.
- Misconfigurations that could cause resource abuse or instability.
- Security flaws in the agent's own architecture (e.g., data exposure, log leaks).

**Please do not open a public issue.** Instead, report the vulnerability via email to:

**[thirstyworld78@gamil.com]**   <!-- Replace with your actual contact email -->

We will acknowledge your report within 48 hours and provide a timeline for resolution. We practice coordinated disclosure; once a fix is ready, we will credit you (if desired) in the release notes.

## Responsible Use

Omni is designed for **authorized security testing only**. You must:

- Obtain explicit, written permission from the target owner before running any scans.
- Comply with the scope, rate limits, and rules of engagement of any bug bounty program you participate in.
- Never use Omni for unauthorized, illegal, or malicious purposes.

The agent includes built-in ethical guardrails (scope enforcement, Safe Mode, rate limiting), but **you** are ultimately responsible for the commands you execute.

## Supported Versions

| Version | Status           |
|---------|------------------|
| v5.0    | :white_check_mark: Actively supported |
| < v5.0  | :x: No longer supported |

We recommend always using the latest version of the `agent.md` from the `main` branch to ensure all safety features are present.

## Security Practices for Users

- **Review the scope:** Always define a clear target scope in your prompt.
- **Use Safe Mode (default):** Do not enable Aggressive Mode unless you fully understand the risks and have the authority to perform deeper exploitation.
- **Monitor sessions:** Keep an eye on long-running scans and use the built-in health check warnings.
- **Secure credentials:** Never hardcode credentials in prompts. Provide them interactively when asked by the agent.
- **Log sanitization:** The agent saves raw output logs to `./logs/`. Ensure these files do not contain sensitive data before sharing or archiving.

## Acknowledgments

We thank the security community for responsibly disclosing any issues. A list of credited researchers can be found in our [ACKNOWLEDGMENTS](ACKNOWLEDGMENTS) file.
