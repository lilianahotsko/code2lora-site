# code2lora.app

Product landing page for **Code2LoRA**: repository knowledge compiled into a
small adapter for open-weight coding models. Zero extra tokens per request,
per-commit updates, fully on-prem.

The research project page (paper, benchmark tables, citation) lives separately at
https://lilianahotsko.github.io/Code2LoRA/.

## Structure

A single static `index.html` (no build step) served by GitHub Pages on the
`code2lora.app` custom domain (`CNAME`). Edit, commit, push; Pages redeploys
automatically.

Page sections, in order: hero, problem, how it works (Snapshot and Live engines),
solutions (persona tabs), savings calculator, proof (paper numbers), security,
plans and fit matrix, why now / traction, CLI, FAQ, final CTA.

- Persona deep links: `#for-leaders`, `#for-devtools`, `#for-consultancies`, `#for-msps`
  (these open the matching tab and load the matching calculator preset).
- Calculator presets: `PRESETS` in the inline script at the bottom of `index.html`.
- Contact address: `hello@code2lora.app` (search and replace to change it).
- Benchmark numbers come from the paper's `tables/numbers-headline.tex` and
  `tables/table-efficiency.tex`; update both pages together when they change.

## Custom domain

DNS is on Cloudflare: apex A records to GitHub Pages
(`185.199.108.153`–`185.199.111.153`) and `www` CNAME to `lilianahotsko.github.io`,
with the same proxy setting on both and SSL/TLS mode **Full**.

## License

MIT.
