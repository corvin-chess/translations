<div align="center">

<a href="https://github.com/corvin-chess"><img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0b0d12,55:161b2b,100:2f3d63&text=Corvin&fontColor=e6e9f2&fontSize=64&fontAlignY=45&animation=twinkling" alt="Corvin" width="100%" /></a>

<img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=500&size=16&color=8FA3D9&center=true&vCenter=true&width=560&height=34&duration=2800&pause=1200&lines=translations;en+and+it+play-shell+locale+files;Planned+full+catalog+and+packages." alt="translations" />

<p>
  <a href="https://github.com/corvin-chess/translations"><img src="https://skillicons.dev/icons?i=github&theme=dark" width="44" height="44" alt="translations" /></a>&nbsp;
  <a href="https://github.com/corvin-chess"><img src="https://skillicons.dev/icons?i=github&theme=dark" width="44" height="44" alt="GitHub" /></a>
</p>

</div>

<br/>

en and it play-shell locale files for lobby, game, and offers. Planned: full catalog and packages.

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=18&color=8FA3D9&center=true&vCenter=true&width=420&height=40&duration=1&pause=1000000&letterSpacing=6px&lines=OVERVIEW" alt="Overview" /></p>

Corvin UI locale sources for [web](https://github.com/corvin-chess/web), [mobile](https://github.com/corvin-chess/mobile), and [website](https://github.com/corvin-chess/website). Day-one locales are en and it with matching key sets. This repository currently ships `en/play-shell.json` and `it/play-shell.json` covering lobby, in-game, and offer strings for the play shell. Broader catalogs and publishable packages remain Planned.

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=18&color=8FA3D9&center=true&vCenter=true&width=420&height=40&duration=1&pause=1000000&letterSpacing=6px&lines=GETTING+STARTED" alt="Getting Started" /></p>

```bash
git clone https://github.com/corvin-chess/translations.git
cd translations
```

Locale files:

- `en/play-shell.json`
- `it/play-shell.json`

Clients load JSON by locale code. Interpolation uses `{{name}}` placeholders (for example `game.moveAnnounced` and `game.ratingDiff`).

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=18&color=8FA3D9&center=true&vCenter=true&width=420&height=40&duration=1&pause=1000000&letterSpacing=6px&lines=DEVELOPMENT" alt="Development" /></p>

Contributor workflow:

1. Add or change keys in `en/` first.
2. Mirror every key in `it/` in the same commit (identical trees).
3. Keep string leaves non-empty, without emoji, and without placeholder copy.
4. Keep `{{placeholder}}` names identical across locales.
5. Run `node scripts/verify-locales.mjs` before opening a pull request.

Do not invent coverage percentages or claim unpublished locales.

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=18&color=8FA3D9&center=true&vCenter=true&width=420&height=40&duration=1&pause=1000000&letterSpacing=6px&lines=TESTING" alt="Testing" /></p>

```bash
node scripts/verify-locales.mjs
node scripts/verify-readme.mjs
```

`verify-locales.mjs` checks JSON parse, en/it key parity, required lobby/game/offers keys, non-empty leaves, matching placeholders, and that Italian is not a near-copy of English.

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=18&color=8FA3D9&center=true&vCenter=true&width=420&height=40&duration=1&pause=1000000&letterSpacing=6px&lines=ARCHITECTURE" alt="Architecture" /></p>

Flat locale trees `en/` and `it/` hold JSON catalogs with no runtime. Play-shell copy is namespaced under `lobby`, `game`, and `offers` to match PROTOCOL.md surfaces consumed by play clients. See organization ADRs and [website](https://github.com/corvin-chess/website) once docs are published.

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=18&color=8FA3D9&center=true&vCenter=true&width=420&height=40&duration=1&pause=1000000&letterSpacing=6px&lines=STATUS" alt="Status" /></p>

| Area | State |
|---|---|
| README | Built |
| LICENSE | Built |
| CI verify gate | Built |
| en play-shell (lobby/game/offers) | Built |
| it play-shell (lobby/game/offers) | Built |
| Key parity checks | Built |
| Contributor workflow | Built |
| Full locale catalog | Planned |
| Publishable packages | Planned |
| Implementation | Planned |

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:0b0d12,35:8fa3d9,70:c9a227,100:0b0d12" width="100%" alt="" />

<br/>

<p align="center"><sub><i>Every UI string ships in en and it together so the board speaks the same truth everywhere.</i></sub></p>

## License

This repository is licensed under CC BY-SA 4.0.

<img src="https://capsule-render.vercel.app/api?type=waving&section=footer&height=110&color=0:0b0d12,55:161b2b,100:2f3d63" alt="" width="100%" />
