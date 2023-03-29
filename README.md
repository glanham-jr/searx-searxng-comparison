# Comparison of searx to SearxNG 

This README document aims to cover the main differences between [searx](https://github.com/searx/searx) and [SearxNG](https://github.com/searxng/searxng). This document does not aim to provide an opinion on which project to choose.

If there are any mistakes or ambiguities in this document, feel free to open a pull request.

## Brief

SearxNG has more features, plugins, engines, and language support. Bug fix turnaround time is generally faster. Also includes an updated user interface w/ Dark Mode and server metrics. searx has a stable codebase with less bugs (though engine integrations can still break), and now focuses engine/plugin integrations with a stricter stance on user privacy violations.

## Details

SearxNG is a fork of searx. At some point, a number of maintainers thought that new proposed features (specifically engine metrics) would encroach on user privacy, while others did not. Therefore, SearxNG was forked so that these features could be accepted. The searx and SearxNG project have not formally defined what constitutes a user privacy violation.

While the searx README states it is not in maintenance mode, any major changes to the codebase are not generally accepted. Overall, the project appears to be considered "complete", and mainly engines addition/maintanence, plug-in addition/maintanence, or bug fixes are occuring at this time. 

SearxNG is significantly much more active, based on the number of accepted pull requests into the project. With this, its expected that the code base is accepting changes to support features accepted by the maintainers. 

One aspect of searx and SearxNG is that they both rely on integrating with third party engines. These engines may or may not provide proper APIs or support for integration (i.e. may involve scraping sites). Therefore, engine integrations occasionally break as the source engine updates their end. With this, SearxNG generally has a faster engine integration fix speed than searx.

## Comparison Tables

These comparison tables do not include all possible comparisons between the two projects, but may provide a quick details that are important in making a decision.

| Project Structure | searx      | SearxNG |
| ----------------- | ---------- | ------- |
| Release Cycle     | Stable     | Fast    |
| New Features      | Yes?[^1]   | Yes     |
| New Engines       | Yes        | Yes     |


| Features                        | searx            | SearxNG              |
| ------------------------------- | ---------------- | -------------------- |
| Meta-Searching 	          | Yes              | Yes                  |
| Telemetry      	          | No               | No                   |
| Server Metrics 	          | No               | Yes[^2]              |
| Translations   	          | Yes              | Yes w/ More Coverage |
| JavaScript     	          | Not Required     | Not Required         |
| Image Proxy    	          | Yes w/ [Morty](https://searx.github.io/searx/utils/filtron.sh.html) | Yes |
| Bot Blocker    	          | Yes w/ [Filtron](https://searx.github.io/searx/utils/morty.sh.html) | Yes |
| Url Blocker/Replacer            | No               | Yes                  |
| Dark Mode                       | No               | Yes                  |
| Right-to-Left Language Support  | No               | Yes                  |

[^1]: Excludes possible user privacy violations deemed by searx maintainers.

[^2]: Opt-in by default. Can be [disabled on the server](https://docs.searxng.org/admin/engines/settings.html#general)
