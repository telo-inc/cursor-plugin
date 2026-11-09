# Telo for Cursor

![Telo](assets/icon.png)

Explore your Apple Health history with telo. This plugin brings two guided workflows to Cursor: a weekly review of sleep, activity and workouts, and longer-term comparisons across months or years. Both explain missing records and compare your own history without turning gaps into zeros.

## Get started

Requires an iPhone with the [telo app](https://telo.health). Sign in to telo, allow access to the Apple Health records you want to share, and complete “Send history to telo” before asking Cursor about your data. Use the same telo account when connecting in Cursor.

This repository is the plugin package. A Cursor Marketplace listing is not yet available.

To try it locally, clone this repository and use Cursor's **Customize → Plugins → Import from Disk**, selecting the repository folder. Authenticate the telo MCP server through Cursor's OAuth flow. No API key, terminal process or health export is required. Local plugin imports may be restricted by your team's policy.

Free includes the last seven days of history. Pro unlocks older synced history; comparisons requiring earlier records depend on your plan and data coverage.

## Try these prompts

- “Give me my weekly health review, including missing data and comparison with the previous seven days.”
- “How have my available health metrics changed over the last year?”
- “What health data has reached telo, and how recent is it?”

The first two prompts use the bundled skills. Data availability can also be inspected directly through the connector. Answers follow the language of your request.

## What the plugin does

The plugin contains Markdown instructions and one remote MCP connector at https://telo.health/mcp. It queries the health records synced to your connected telo account, including daily metrics, sleep and workout sessions, personal baselines and data availability. Relevant results are returned to Cursor to answer your request. The telo service records access metadata in your account history. The plugin adds no executable scripts, hooks, local services or additional external data destinations.

Queries do not modify health records. Data availability depends on the records accessible to the iPhone app and the uploads received by telo. The plugin cannot verify HealthKit read permissions or that a history import has finished. It does not diagnose conditions or recommend treatment.

## Skills

- **Weekly health review:** compares the last seven complete local days with the preceding seven days, reports coverage, and uses available personal baselines.
- **Long-term trends:** compares weekly or monthly aggregates with explicit dates, units and observed days; handles gaps and truncated responses.

[Website](https://telo.health) · [Privacy](https://telo.health/privacy) · [Terms](https://telo.health/terms) · [Support](mailto:contact@telo.health)

The MIT license covers this plugin's instructions and configuration. The telo service remains subject to its own terms. Telo names and branding are not granted as trademarks by the plugin license.
