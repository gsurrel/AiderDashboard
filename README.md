# AiderDashboard

This is a dashboard to [visualize]([url](https://gsurrel.github.io/AiderDashboard/)) the [Aider LLM leaderboard](https://aider.chat/docs/leaderboards/), using the data [straight from the repository](https://github.com/Aider-AI/aider/blob/main/aider/website/_data/polyglot_leaderboard.yml).

The visualization is done purely on the client's side, with a single [Vega-Lite]([url](https://vega.github.io/vega-lite/)) specification.

The page _and_ visualization color-scheme follow the user's current theme (dark/light) using [barely known CSS colors](https://developer.mozilla.org/en-US/docs/Web/CSS/system-color). Kudos to Firefox for using the user's selected hue for tuning the `AccentColor`, and have a super-nice blending-in the OS (and I'm not so sure it's a security concern as most people do not change their theme at all, so using the default one is already very damaging).

**Note:** Vega cannot load YAML data, and I do not perform any pre-processing. This means that I chain many [transforms]([url](https://vega.github.io/vega-lite/docs/transform.html)) to "parse" the YAML to proper objects. It's dirty code, but hey, it works!
