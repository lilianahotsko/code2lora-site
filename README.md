# Code2LoRA — project website

Static project page for **Code2LoRA: Hypernetworks for Repository-Conditioned and
Commit-Streaming Adapters of Code Language Models** and its EMNLP 2026 system
demonstration, **c2l-terminal**.

Deployed via GitHub Pages on a custom domain.

## What Code2LoRA is

A hypernetwork trained once, across hundreds of repositories, that maps a
repository's commit history directly to a LoRA adapter for a frozen code LLM
(Qwen2.5-Coder-1.5B) — repository knowledge with zero inference-time token
overhead, updated in O(1) per commit.

**c2l-terminal** packages it as a pip-installable, offline-capable terminal
coding assistant:

```bash
pip install code2lora      # https://pypi.org/project/code2lora/
```

## Links

| | |
|---|---|
| PyPI package | https://pypi.org/project/code2lora/ |
| Terminal tool (source) | https://github.com/lilianahotsko/c2l_terminal |
| Live browser demo | https://huggingface.co/spaces/code2lora/code2lora-gru-demo |
| Checkpoint (GRU) | https://huggingface.co/code2lora/code2lora-gru |
| Checkpoint (Static) | https://huggingface.co/code2lora/code2lora-direct |
| Benchmark datasets | https://huggingface.co/datasets/code2lora/code2lora-static · https://huggingface.co/datasets/code2lora/code2lora-evo |

## Custom domain setup

1. Add a `CNAME` file at the repo root containing your domain (e.g. `code2lora.com`).
2. In **Settings → Pages → Custom domain**, enter the same domain.
3. At your registrar, point DNS to GitHub Pages:
   - **Apex (`@`)**: A records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **`www`**: CNAME → `lilianahotsko.github.io`
4. Enable **Enforce HTTPS** once the certificate is issued.

## Editing the site

The site is a single static `index.html` (no build step) served by GitHub
Pages from the `main` branch. Edit, commit, push — Pages redeploys
automatically.

When the demo video is published, replace the placeholder in the
`#video-slot` div with the YouTube `<iframe>` embed (instructions are in an
HTML comment at that spot).

## License

MIT.
