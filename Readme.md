# CleanStart Container for Go

Official Go programming language container image optimized for enterprise environments. Includes the complete Go development toolkit, compiler, and runtime environment. Features security-hardened base image, minimal attack surface, and FIPS-compliant cryptographic modules. Supports both production deployments and development workflows with separate tagged versions. Includes standard Go tools like go test, go fmt, and go mod for dependency management. The CleanStart Go image provides a complete development and runtime environment optimized for enterprise applications. Built with security hardening and comprehensive tooling, this image delivers reliable application execution with advanced security features.

**📌 CleanStart Foundation:** Security-hardened, minimal base OS designed for enterprise containerized environments.

**Image Path:** `ghcr.io/cleanstart-containers/go`

**Registry:** CleanStart Registry

---

## Overview

This Go container provides a complete Go programming language development and runtime environment. It includes the Go compiler, standard library, and essential development tools, designed for both development and production use cases. This CleanStart Go container is part of the CleanStart runtime suite, featuring enterprise-grade security hardening, automated vulnerability management, and compliance with industry standards.

---

## About CleanStart

CleanStart is a comprehensive container registry providing security-hardened, enterprise-ready container images. Our images are designed with security-first principles, featuring minimal attack surfaces, regular security updates, and compliance with industry standards.

### About CleanStart Images

CleanStart images are built on secure, minimal base operating systems and optimized for production environments. Each image undergoes rigorous security testing, vulnerability scanning, and compliance validation to ensure enterprise-grade security and reliability.

---

## Key Features

- **Security-First Design**: Built with minimal attack surfaces and security hardening
- **Enterprise Compliance**: Meets industry standards including FIPS, STIG, and CIS benchmarks
- **Regular Updates**: Automated security patches and vulnerability management
- **Multi-Architecture Support**: Available for AMD64 and ARM64 architectures
- **Production Ready**: Optimized for enterprise deployment and scaling
- **Comprehensive Documentation**: Detailed guides and best practices for each image
- Complete Go development environment with compiler and standard library
- Optimized for cloud-native and microservices architectures
- Standard Go tools (go test, go fmt, go mod) included
- FIPS-compliant cryptographic modules
- Separate tags for development and production

---

## Common Use Cases

Typical scenarios where this container excels:

- Building and deploying Go microservices
- Cloud-native application development
- API development and deployment
- Backend services and distributed systems
- CLI tools and utilities development
- Container-based CI/CD pipelines

---

## Quick Start

### Pull Commands

Download the runtime container images:
```bash
docker pull ghcr.io/cleanstart-containers/go:latest
```
```bash
docker pull ghcr.io/cleanstart-containers/go:latest-dev
```

### Interactive Development

Start interactive session for development:
```bash
docker run --rm -it --entrypoint /bin/sh ghcr.io/cleanstart-containers/go:latest-dev
```

You should be inside container shell, execute commands like:
```bash
whoami
```
```bash
pwd
```
```bash
ls
```
```bash
exit
```

### Container Start

Start the container:
```bash
docker run --rm -it --name go-web-dev ghcr.io/cleanstart-containers/go:latest
```

### Development Workflow

Run with workspace mounted:
```bash
docker run -it --name go-dev \
  -v $(pwd):/workspace \
  -w /workspace \
  --entrypoint /bin/sh \
  ghcr.io/cleanstart-containers/go:latest-dev
```

Check Go version:
```bash
docker run --rm ghcr.io/cleanstart-containers/go:latest-dev go version
```

---

## Best Practices

- Use specific image tags for production (avoid latest)
- Configure resource limits: memory and CPU constraints
- Enable read-only root filesystem when possible
- Mount source code as volumes for development
- Use multi-stage builds for production images
- Leverage Go modules for dependency management

---

## Architecture Support

CleanStart images support multiple architectures to ensure compatibility across different deployment environments:

- **AMD64**: Intel and AMD x86-64 processors
- **ARM64**: ARM-based processors including Apple Silicon and ARM servers

### Multi-Platform Images
```bash
docker pull --platform linux/amd64 ghcr.io/cleanstart-containers/go:latest
```
```bash
docker pull --platform linux/arm64 ghcr.io/cleanstart-containers/go:latest
```

---

## Resources & Documentation

### Essential Links

- **CleanStart Website:** https://www.cleanstart.com
- **Go Official:** https://go.dev/
- **Go Documentation:** https://go.dev/doc/

### Reference

- **CleanStart All Images:** https://images.cleanstart.com
- **CleanStart Community Images:** https://hub.docker.com/u/cleanstart
- **View Provenance, Specifications, SBOM, Signature:** https://images.cleanstart.com/images/go
- **Other location for Community image:** https://hub.docker.com/r/cleanstart/go

---

## Vulnerability Disclaimer

CleanStart offers Docker images that include third-party open-source libraries and packages maintained by independent contributors. While CleanStart maintains these images and applies industry-standard security practices, it cannot guarantee the security or integrity of upstream components beyond its control.

Users acknowledge and agree that open-source software may contain undiscovered vulnerabilities or introduce new risks through updates. CleanStart shall not be liable for security issues originating from third-party libraries, including but not limited to zero-day exploits, supply chain attacks, or contributor-introduced risks.

**Security remains a shared responsibility:** CleanStart provides updated images and guidance where possible, while users are responsible for evaluating deployments and implementing appropriate controls.
