# GitBundle

## What is GitBundle?

[GitBundle](https://gitbundle.com) is a cloud-native, plugin-driven, out-of-the-box, self-hosted, modern Git service program. It is similar to GitHub, Bitbucket, and GitLab.
[GitBundle](https://gitbundle.com) is a fork of [Gitea](https://gitea.com). It also provides a one-click plug-in management service, such as [Bundle-Builds](https://plugin-docs.gitbundle.com/bundle-builds/overview/), [Bundle-Deployments](https://plugin-docs.gitbundle.com/bundle-deployments/overview/), [Bundle-Pods](https://plugin-docs.gitbundle.com/bundle-pods/overview/), [Bundle-Metrics](https://plugin-docs.gitbundle.com/bundle-metrics/overview/) components.

## Purpose

The goal of this project is to provide the easiest, fastest, and most painless way of setting
up a self-hosted Git service including CI/CD, Docker, Kubernetes. 
With Go, this can be done with an independent binary distribution
across all platforms and architectures that Go supports. This support includes Linux, macOS, and
Windows, on architectures like amd64, arm64, and others.

## Features &&nbsp;[Pricing](https://gitbundle.com/pricing)

- Support event timeline
- Supports SSH and HTTP/HTTPS
- Supports SMTP, LDAP, and reverse proxy user authentication
- Supports reverse proxy subpaths
- Support user, organization and warehouse management systems
- Support for adding and removing warehouse collaborators
- Support for warehouse and organization-level Web hooks (including Slack integration)
- Support for repository Git hooks and deployment keys
- Support warehouse issues, Pull requests, and wikis
- Support for migrating and mirroring repositories and their wikis
- Supports online editing of repository files and wikis
- Supports custom source Gravatar and Federated Avatar
- Support mail service
- Support background management panel
- Supports MySQL, PostgreSQL, SQLite3, MSSQL, and TiDB(MySQL) databases
- support package registry (Composer/Conan/Container/Generic/Helm/Maven/NPM/Nuget/PyPI/RubyGems)
- Supports one-click installation of plug-ins (Bundle-builds/Bundle-deployments/Bundle-pods/Bundle-metrics)
- Support multi-cluster Kubernetes management, support Pods, Metrics, Deployments, Services, HPA and other functions
- Support for warehouse deployment testing, deployment rollback, deployment lock-in, and pre-release validation (based on Kubernetes microservice clusters, implemented using Bundle-deployments)
- Allows site administrators to configure the CPU/Memory resources available to the organization (Kubernetes cluster quota)
- Allows site administrators to configure the list of plug-ins available to the organization/repository
- Allows site administrators to configure organizations to enable software registries

## System Requirements

- A Raspberry Pi 3 is powerful enough to run GitBundle for small workloads.
- 2 CPU cores and 1GB RAM is typically sufficient for small teams/projects.
- GitBundle should be run with a dedicated non-root system account on UNIX-type systems.
   - Note: GitBundle manages the `~/.ssh/authorized_keys` file. Running GitBundle as a regular user could break that user's ability to log in.
- [Git](https://git-scm.com/) version 2.0.0 or later is required.
   - [Git Large File Storage](https://git-lfs.github.com/) will be available if enabled when Git >= 2.1.2.
   - Git commit-graph rendering will be enabled automatically when Git >= 2.18.

## Browser Support

- Last 2 versions of Chrome, Firefox, Safari and Edge
- Firefox ESR

## Components

* Web server framework: [Chi](http://github.com/go-chi/chi)
* ORM: [XORM](https://xorm.io)
* UI frameworks:
  * [jQuery](https://jquery.com)
  * [Tailwindcss](https://tailwindcss.com)
  * [Svelte](https://svelte.dev)
  * [React](https://react.dev/)
  <!-- * and various components (see package.json) -->
* Editors:
  * [CodeMirror](https://codemirror.net)
  * [EasyMDE](https://github.com/Ionaru/easy-markdown-editor)
  * [Monaco Editor](https://microsoft.github.io/monaco-editor)
* Database drivers:
  * [github.com/go-sql-driver/mysql](https://github.com/go-sql-driver/mysql)
  * [github.com/lib/pq](https://github.com/lib/pq)
  <!-- * [github.com/denisenkom/go-mssqldb](https://github.com/denisenkom/go-mssqldb) -->

## Plugins Support

- [Bundle-builds](https://plugin-docs.gitbundle.com/bundle-builds) (Built-In CI/CD)
- [Bundle-deployments](https://plugin-docs.gitbundle.com/bundle-deployments) (Built-In CD For Kubernetes)
- [Bundle-pods](https://plugin-docs.gitbundle.com/bundle-pods) (Built-In For Kubernetes Pods)
- [Bundle-metrics](https://plugin-docs.gitbundle.com/bundle-metrics) (Built-In For Kubernetes Pods)