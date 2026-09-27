<div align="center">

<a href="https://dorkforge.github.io/">
  <img src="https://dorkforge.github.io/assets/icon-192.png" alt="DorkForge logo" width="96" height="96" />
</a>

# DorkForge

**Open, privacy‑first tooling for search‑engine reconnaissance and attack‑surface review.**

We build free, browser‑based utilities that help defenders find what search engines have indexed by mistake, so it gets fixed before anyone else finds it.

[![Website](https://img.shields.io/badge/website-dorkforge.github.io-0d8ba0?style=flat-square&logo=googlechrome&logoColor=white)](https://dorkforge.github.io/)
[![Deploy](https://img.shields.io/github/actions/workflow/status/DorkForge/DorkForge.github.io/static.yml?branch=main&style=flat-square&label=deploy&logo=githubactions&logoColor=white)](https://github.com/DorkForge/DorkForge.github.io/actions/workflows/static.yml)
[![Stars](https://img.shields.io/github/stars/DorkForge/DorkForge.github.io?style=flat-square&logo=github&label=stars)](https://github.com/DorkForge/DorkForge.github.io/stargazers)
[![Price](https://img.shields.io/badge/price-free-2ea44f?style=flat-square)](https://dorkforge.github.io/)
[![Data collected](https://img.shields.io/badge/data%20collected-none-5a0fc8?style=flat-square)](https://github.com/DorkForge/DorkForge.github.io#-privacy)

[**Website**](https://dorkforge.github.io/) &nbsp;·&nbsp;
[**Projects**](#projects) &nbsp;·&nbsp;
[**Principles**](#principles) &nbsp;·&nbsp;
[**Contributing**](#contributing) &nbsp;·&nbsp;
[**Security**](#security) &nbsp;·&nbsp;
[**Responsible use**](#responsible-use)

</div>

---

## About

Search engines index far more than their owners intend: configuration files, backups, logs, admin panels and forgotten staging hosts. The operators that surface this exposure (`site:`, `filetype:`, `intitle:`, `inurl:` and friends) are powerful but easy to get wrong.

**DorkForge** makes that work precise, repeatable and safe. Our tools run entirely in the browser, store nothing on a server, and are built around one goal: **helping the people responsible for a system see it the way an attacker's search results would.**

## Projects

<table>
<tr>
<td width="58%" valign="top">

### [DorkForge: Google Dork Builder](https://github.com/DorkForge/DorkForge.github.io)

A mobile‑first builder for advanced search queries, often called *Google dorks*.

- **Visual builder** for `site:`, `intitle:`, `inurl:`, `intext:`, `filetype:`, `before:`/`after:`, number ranges and `OR` groups
- **12 GHDB presets** and a **curated library** of 24 tagged dorks
- **Query linting** that flags broken, conflicting or unscoped queries
- **Plain‑English explain** mode that reads any query back as a sentence
- **One‑tap search** on Google, Bing and DuckDuckGo, with engine‑aware operator handling
- **Local history**, saved queries, CSV export and shareable deep links
- **Installable PWA** with light, dark and auto themes

<p>
  <a href="https://dorkforge.github.io/"><b>Launch the app →</b></a> &nbsp;·&nbsp;
  <a href="https://github.com/DorkForge/DorkForge.github.io"><b>View source →</b></a>
</p>

<sub><b>Status:</b> Active &nbsp;·&nbsp; <b>Stack:</b> HTML, CSS, vanilla JS &nbsp;·&nbsp; <b>Dependencies:</b> 0 &nbsp;·&nbsp; <b>Hosting:</b> GitHub Pages</sub>

</td>
<td width="42%" valign="top" align="center">

<a href="https://dorkforge.github.io/">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/DorkForge/DorkForge.github.io/main/.github/assets/screenshot-build-dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/DorkForge/DorkForge.github.io/main/.github/assets/screenshot-build-light.png" />
    <img src="https://raw.githubusercontent.com/DorkForge/DorkForge.github.io/main/.github/assets/screenshot-build-dark.png" alt="DorkForge Build tab showing a syntax-highlighted query" width="230" />
  </picture>
</a>

</td>
</tr>
</table>

**Example.** Find exposed environment files on a domain you are authorized to test:

```text
site:example.com (filetype:env OR filetype:conf) intext:DB_PASSWORD -sample
```

> More tools are on the roadmap. Watch this organization or [open an issue](https://github.com/DorkForge/DorkForge.github.io/issues/new) to suggest what we should build next.

## Principles

| Principle | What it means in practice |
|---|---|
| **Defense first** | Every tool is designed to help owners find and fix exposure. Guardrails nudge users to scope queries to assets they are authorized to test. |
| **Private by default** | No accounts, no backend, no analytics, no cookies. Your queries and history stay in your browser. |
| **Zero friction** | Static sites with no install, no sign‑up and no build step. They open instantly on any device. |
| **Simple and auditable** | Small, dependency‑free code you can read in one sitting and self‑host with a single command. |
| **Open by default** | Built in public. Issues, ideas and pull requests are welcome. |

## Who it's for

| Audience | Typical use |
|---|---|
| **Security and blue teams** | Periodic reviews of what an organization's domains expose to search engines |
| **Penetration testers** | Passive reconnaissance during scoped, authorized engagements |
| **Bug bounty hunters** | Discovery work that stays inside a program's published scope |
| **OSINT researchers** | Building precise, reproducible search queries |
| **Site owners and sysadmins** | Checking for leaked configs, backups, logs and admin panels |
| **Students and educators** | Learning how search operators work, with explanations built in |

## Contributing

We welcome contributions of every size.

- **Star** [DorkForge.github.io](https://github.com/DorkForge/DorkForge.github.io) to follow development.
- **Suggest** a preset, library dork or feature by [opening an issue](https://github.com/DorkForge/DorkForge.github.io/issues/new).
- **Contribute code** by following the [contributing guide](https://github.com/DorkForge/DorkForge.github.io#-contributing) and opening a pull request.

New dorks should target *exposure discovery* (misconfigurations an owner would want to fix), stay generic and scope‑able with `site:`, and never reference real target domains or aim primarily at harvesting personal data.

## Security

If you find a vulnerability in any DorkForge project, please report it **privately** through [GitHub Security Advisories](https://github.com/DorkForge/DorkForge.github.io/security/advisories/new) rather than opening a public issue.

## Responsible use

> [!IMPORTANT]
> DorkForge tools generate search queries. They do not scan, crawl, access or download anything. Only run exposure queries against assets you **own or are explicitly authorized to test**, and treat every result as something to report and remediate, never to exploit. You are responsible for complying with applicable law, your organization's policies and the rules of any program you take part in.

---

<div align="center">

<sub>
  <a href="https://dorkforge.github.io/">dorkforge.github.io</a> &nbsp;·&nbsp;
  Free, private and client‑side &nbsp;·&nbsp;
  Built for defenders
</sub>

</div>
