# hexbytescanner-hooks
Old school json hooks for [hexbytescanner](https://github.com/karek314/hexbytescanner)

This repository contains multiple different json hooks/tasks for [hexbytescanner](https://github.com/karek314/hexbytescanner) running on MacOS. It's useful when symbols are stripped from binary, rendering method swizzling by symbols not possible.

## Hooks/Tasks

<b>openssl_hook.json</b> - OpenSSL 1.0.2 certificate pinning hook on arm64.<br>
<b>openssl_hook_v2.json</b> - OpenSSL 1.0.2 certificate pinning hook on arm64, improved pattern, possibly for different compiler version or slighlty updated OpenSSL, use if first version does not find patch location.<br>
These hooks patch call to <b>ssl_verify_cert_chain</b> in <b>ssl3_get_server_certificate</b>.<br>
<b>openssl_1_1_0_hook.json</b> OpenSSL 1.1.0 certifiate pinning hook for arm64, it modifies cmp instruction in <b>tls_process_server_certificate</b> method.


## Contributing
If you find useful/interesting hooks, please submit pr with it. If this is update for already existing hook, please append task in related .json file if it isn't colliding with old ones.


## Disclaimer / Warning
This repository/project is intended for educational purposes ONLY. It is not intended to be used for any purpose other than learning, so please do not use it for any other reason.

## License
MIT
