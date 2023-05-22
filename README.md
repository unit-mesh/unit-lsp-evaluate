# Unit Agent

[![Build](https://github.com/unit-mesh/unit-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/unit-mesh/unit-agent/actions/workflows/ci.yml)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/unit-mesh/unit-lsp-server)

Todos:

- [x] TreeSitter parser for unit
    - [x] based on: [https://github.com/BloopAI/bloop/tree/main](https://github.com/BloopAI/bloop/tree/main)
- [x] Json RPC server with [xi-rpc](https://crates.io/crates/xi-rpc)
    - [x] CLI
- [ ] Support completion type
    - [ ] Inline
    - [ ] AfterLineEnd
    - [ ] Block

Support for IDE features:

- [ ] Chat with IDE
  - [ ] Generate test
  - [ ] 实现：`重现 xx 功能`, `devti:/chat/feature`
  - [ ] 重构：`重构 xx 方法`
  - [ ] 替换：`替换 xx 方法`，`devti:/refactor/method`
- [x] Custom LLM Server
- [ ] Telemetry Server
  - [ ] Accept
  - [ ] Reject
  - [ ] Feedback
- [ ] Context Engineering
  - [ ] Open Tabs
  - [ ] Related Files
  - [ ] with Dependency Context
    - [ ] parse Gradle for dependencies
- [ ] Local Model  
  - [ ] Local Embedding / Model with Onnx ?
  - [ ] Local Conversation converter.
  - [ ] Max Token Usage with Model specific ?

## JSON RPC Protocol

- Notifications
  - `client_started` or `initialize`
  - notify/show
  - notify/accepted
  - notify/rejected
  - workspace/dependencies
  - workspace/file-open
  - workspace/file-change
  - workspace/file-close
- Request
  - config 
  - status/get
  - editor/info
  - version/get
  - completion/once
  - completion/cycling
  - completion/solutions

## LICENSE

This code is distributed under the Apache 2.0 license. See `LICENSE` in this directory.
