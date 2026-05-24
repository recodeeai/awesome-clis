# awesome-clis

> Curated list of CLIs used across [cue](https://github.com/recodeee/cue) profiles — the tools behind each AI agent loadout.

Every cue profile declares which skills, MCPs, and CLIs it needs. This repo catalogs every CLI dependency across all profiles so you can see what's required before switching profiles.

## CLIs by Profile

### core (all profiles inherit these)
| CLI | What it does | Install |
|-----|-------------|---------|
| `git` | Version control | `apt install git` |
| `gh` | GitHub CLI — PRs, issues, repos | `apt install gh` |
| `curl` | HTTP requests | `apt install curl` |
| `jq` | JSON processing | `apt install jq` |
| `python3` | Python runtime for MCP servers | `apt install python3` |

### backend
| CLI | What it does | Install |
|-----|-------------|---------|
| `npx` | Run npm packages without install | comes with `npm` |
| `docker` | Containers | `apt install docker.io` |
| `aws` | AWS CLI | `pip install awscli` |

### frontend
| CLI | What it does | Install |
|-----|-------------|---------|
| `npx` | Run npm packages | comes with `npm` |
| `convert` | ImageMagick — image processing | `apt install imagemagick` |

### creative-media
| CLI | What it does | Install |
|-----|-------------|---------|
| `ffmpeg` | Video/audio processing | `apt install ffmpeg` |
| `cairosvg` | SVG to PNG rendering | `pip install cairosvg` |
| `convert` | ImageMagick | `apt install imagemagick` |
| `higgsfield` | AI video generation | [higgsfield.ai](https://higgsfield.ai) |

### marketing
| CLI | What it does | Install |
|-----|-------------|---------|
| `gh` | GitHub PRs for awesome-list submissions | `apt install gh` |
| `curl` | API calls to X/Reddit | `apt install curl` |
| `npx` | Reddit MCP server | comes with `npm` |

### cybersecurity
| CLI | What it does | Install |
|-----|-------------|---------|
| `nmap` | Network scanning | `apt install nmap` |
| `wireshark` | Packet analysis | `apt install wireshark` |
| `ghidra` | Reverse engineering | [ghidra-sre.org](https://ghidra-sre.org) |
| `frida` | Dynamic instrumentation | `pip install frida-tools` |
| `nikto` | Web vulnerability scanner | `apt install nikto` |
| `sqlmap` | SQL injection testing | `apt install sqlmap` |
| `john` | Password cracking | `apt install john` |
| `hashcat` | GPU password cracking | `apt install hashcat` |
| `volatility` | Memory forensics | `pip install volatility3` |
| `autopsy` | Digital forensics | [sleuthkit.org](https://sleuthkit.org/autopsy/) |

### nvidia
| CLI | What it does | Install |
|-----|-------------|---------|
| `python3` | cuOpt API client | `apt install python3` |
| `curl` | API calls to cuOpt server | `apt install curl` |

### coolify
| CLI | What it does | Install |
|-----|-------------|---------|
| `npx` | Coolify MCP | comes with `npm` |
| `curl` | Coolify API | `apt install curl` |

### medusa-dev
| CLI | What it does | Install |
|-----|-------------|---------|
| `npx` | Medusa CLI commands | comes with `npm` |
| `curl` | API testing | `apt install curl` |

### readme-writer
| CLI | What it does | Install |
|-----|-------------|---------|
| `python3` | cairosvg for SVG→PNG | `apt install python3` |
| `cairosvg` | SVG rendering | `pip install cairosvg` |

### research
| CLI | What it does | Install |
|-----|-------------|---------|
| `curl` | Web fetching | `apt install curl` |
| `gh` | GitHub search | `apt install gh` |

### video / creative
| CLI | What it does | Install |
|-----|-------------|---------|
| `ffmpeg` | Video processing, frame extraction | `apt install ffmpeg` |
| `wf-recorder` | Wayland screen recording | `apt install wf-recorder` |
| `grim` | Wayland screenshots | `apt install grim` |
| `cage` | Wayland compositor for headless | `apt install cage` |
| `Xvfb` | Virtual X display | `apt install xvfb` |
| `xdotool` | X11 automation | `apt install xdotool` |
| `kitty` | Terminal with image protocol | [sw.kovidgoyal.net/kitty](https://sw.kovidgoyal.net/kitty/) |
| `tmux` | Terminal multiplexer | `apt install tmux` |
| `tesseract` | OCR | `apt install tesseract-ocr` |

## All CLIs (alphabetical)

| CLI | Used by profiles |
|-----|-----------------|
| `autopsy` | cybersecurity |
| `aws` | backend |
| `cage` | creative-media, video |
| `cairosvg` | creative-media, readme-writer |
| `convert` | frontend, creative-media |
| `curl` | core, backend, coolify, marketing, nvidia, research |
| `docker` | backend |
| `ffmpeg` | creative-media, video |
| `frida` | cybersecurity |
| `gh` | core, marketing, research |
| `ghidra` | cybersecurity |
| `git` | core |
| `grim` | video |
| `hashcat` | cybersecurity |
| `higgsfield` | creative-media |
| `john` | cybersecurity |
| `jq` | core, marketing |
| `kitty` | video |
| `nikto` | cybersecurity |
| `nmap` | cybersecurity |
| `npx` | backend, frontend, coolify, medusa-dev, marketing |
| `python3` | core, nvidia, readme-writer, creative-media |
| `sqlmap` | cybersecurity |
| `tesseract` | video |
| `tmux` | video |
| `volatility` | cybersecurity |
| `wf-recorder` | video |
| `wireshark` | cybersecurity |
| `xdotool` | video |
| `Xvfb` | video |

## Install all (Ubuntu/Debian)

```bash
# Core (required for all profiles)
sudo apt install -y git gh curl jq python3 python3-pip

# Creative/Video
sudo apt install -y ffmpeg imagemagick xvfb xdotool cage grim wf-recorder tmux tesseract-ocr
pip install cairosvg

# Backend
sudo apt install -y docker.io
pip install awscli

# Cybersecurity
sudo apt install -y nmap wireshark nikto sqlmap john hashcat
pip install frida-tools volatility3
```

## Related

- [cue](https://github.com/recodeee/cue) — the profile manager that uses these CLIs
- [cue optimizer](https://github.com/recodeee/cue#cue-optimizer--see-every-loadout-at-a-glance) — visual audit showing CLI install status per profile

## License

MIT
