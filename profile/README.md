<div align="center">
  
  # 🔐 Keyraft
  
  ### Lightweight, Self-Hosted Configuration & Secrets Management
  
  [![GitHub Stars](https://img.shields.io/github/stars/keyraft?style=flat-square&logo=github)](https://github.com/keyraft)
  [![License](https://img.shields.io/badge/license-Apache%202.0-blue?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
  [![Docker Pulls](https://img.shields.io/docker/pulls/keyraft/keyrafted?style=flat-square&logo=docker)](https://hub.docker.com/r/keyraft/keyrafted)
  
  ---
  
  <p>
    <strong>Keyraft</strong> is an open-source configuration and secrets management system designed for teams who want centralized configuration, secure secrets, and live updates without cloud lock-in or heavy operational complexity.
  </p>
  
</div>

## 🎯 Why Keyraft?

| Problem | Keyraft Solution |
|---------|------------------|
| `.env` file chaos across services | Central key-value config store |
| Secret leaks in version control | AES-256-GCM encryption at rest |
| Restart to reload configuration | Watch API for live hot-reload |
| Vendor lock-in to cloud providers | Self-hosted, open protocol |
| Heavy tools (Vault/Consul) | Single binary, minimal dependencies |

## ⚡ Key Features

- **🔑 Secure by Default** - AES-256-GCM encryption for secrets, token-based authentication
- **📦 Simple Deployment** - Single binary, Docker image, no external dependencies
- **🌳 Hierarchical Namespaces** - Organize configs by `project/environment/service`
- **📝 Version Control** - Track every change with full audit history
- **👀 Live Updates** - Watch API for real-time configuration changes
- **🔌 Language Agnostic** - HTTP/JSON API works with any language
- **🎨 Go SDK** - First-class client library with caching and auto-reload

## 🚀 Quick Start

```bash
# Using Docker
docker run -d -p 7200:7200 \
  -v keyraft-data:/data \
  -e KEYRAFT_MASTER_KEY=$(openssl rand -base64 32) \
  keyraft/keyrafted:latest

# Using binary
curl -sSL https://raw.githubusercontent.com/keyraft/keyrafted/main/install.sh | bash
keyrafted init
keyrafted start
```

## 📚 Projects

### [keyrafted](https://github.com/keyraft/keyrafted)
Core server implementation in Go. Single-node configuration and secrets management with BoltDB storage.

**Status:** v0.1 MVP - Production Ready  
**License:** Apache 2.0

### Roadmap

**v0.2** (Next)
- Server-Sent Events (SSE) for watch streaming
- Enhanced audit logging and analytics
- Multi-namespace bulk operations

**v0.3** (Future)
- Raft consensus for clustering
- Multi-node high availability
- Automatic leader election

**v1.0** (Stable)
- Backward compatibility guarantee
- Performance optimizations
- Enterprise features

## 🤝 Contributing

We welcome contributions from the community! Whether you're fixing bugs, adding features, or improving documentation, your help makes Keyraft better.

### Ways to Contribute

- 🐛 **Report bugs** - Open an issue with details
- 💡 **Suggest features** - Share your ideas
- 📖 **Improve docs** - Fix typos, add examples
- 💻 **Submit code** - Fix bugs or implement features
- ⭐ **Star repositories** - Show your support

### Get Started

1. Check out [keyrafted](https://github.com/keyraft/keyrafted) repository
2. Read the [Contributing Guide](https://github.com/keyraft/keyrafted/blob/main/docs/CONTRIBUTING.md)
3. Pick an issue or create a new one
4. Submit a pull request

## 🌟 Community

- **Discussions:** [GitHub Discussions](https://github.com/orgs/keyraft/discussions)
- **Issues:** [GitHub Issues](https://github.com/keyraft/keyrafted/issues)
- **Security:** Report vulnerabilities to xentixar@gmail.com

## 📊 Stats

<div align="center">
  
  ![GitHub Org Stars](https://img.shields.io/github/stars/keyraft?style=for-the-badge&logo=github)
  ![Docker Pulls](https://img.shields.io/docker/pulls/keyraft/keyrafted?style=for-the-badge&logo=docker)
  ![GitHub Contributors](https://img.shields.io/github/contributors/keyraft/keyrafted?style=for-the-badge&logo=github)
  
</div>

## 📄 License

All projects under the Keyraft organization are licensed under the **Apache License 2.0** unless otherwise specified.

---

<div align="center">
  
  **Built with ❤️ for developers who need simple, secure configuration management.**
  
  [Website](https://github.com/keyraft) · [Documentation](https://github.com/keyraft/keyrafted/tree/main/docs) · [Docker Hub](https://hub.docker.com/r/keyraft/keyrafted)
  
</div>

