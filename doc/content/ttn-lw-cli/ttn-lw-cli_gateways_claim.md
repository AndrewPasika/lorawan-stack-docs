---
title: "ttn-lw-cli gateways claim"
slug: ttn-lw-cli_gateways_claim
type: "commands"
---

## ttn-lw-cli gateways claim

Claim a gateway (EXPERIMENTAL)

### Synopsis

Claim an gateway (EXPERIMENTAL)
The claiming procedure transfers ownership of gateways using the Device
Claiming Server.

Gateways need to be authorized for claiming before they can be claimed.
See: "ttn-lw-cli claim authorize"

Authentication of gateway claiming is by the Gateway EUI and the claim
authentication code.
For UDP gateways, the claim authentication code is placed in the gateway
entity, stored in the Identity Server.

As part of claiming, you can optionally provide the target Gateway ID and
Gateway Server address and a frequency plan ID.
For LoRa Basic Station gateways, the Target CUPS URI must be specified.
A PEM encoded CUPS trust may be included in the claim request.


```
ttn-lw-cli gateways claim [gateway-eui] [flags]
```

### Options

```
      --authentication-code string             (hex)
      --gateway-eui string                     
      --gateway-id string                      
  -h, --help                                   help for claim
      --organization-id string                 
      --target-cups-trust-local-file string    (optional) Target CUPS trust in PEM format (local file name)
      --target-cups-uri string                 
      --target-frequency-plan-id string        
      --target-gateway-id string               gateway ID for the claimed gateway
      --target-gateway-server-address string   
      --user-id string                         
```

### Options inherited from parent commands

```
      --allow-unknown-hosts                             Allow sending credentials to unknown hosts
      --application-server-enabled                      Application Server enabled (default true)
      --application-server-grpc-address string          Application Server address (default "localhost:8884")
      --ca string                                       CA certificate file
  -c, --config strings                                  Location of the config files (default [.ttn-lw-cli.yml,$HOME/.ttn-lw-cli.yml,$HOME/.config/.ttn-lw-cli.yml])
      --credentials-id string                           Credentials ID (if using multiple configurations)
      --device-claiming-server-grpc-address string      Device Claiming Server address (default "localhost:8884")
      --device-template-converter-grpc-address string   Device Template Converter address (default "localhost:8884")
      --dump-requests                                   When log level is set to debug, also dump request payload as JSON
      --experimental.features strings                   Experimental features to activate
      --gateway-server-enabled                          Gateway Server enabled (default true)
      --gateway-server-grpc-address string              Gateway Server address (default "localhost:8884")
      --identity-server-grpc-address string             Identity Server address (default "localhost:8884")
      --input-format string                             Input format (default "json")
      --insecure                                        Connect without TLS
      --join-server-enabled                             Join Server enabled (default true)
      --join-server-grpc-address string                 Join Server address (default "localhost:8884")
      --log.format string                               Log format to write (console, json) (default "console")
      --log.level string                                The minimum level log messages must have to be shown (default "info")
      --network-server-enabled                          Network Server enabled (default true)
      --network-server-grpc-address string              Network Server address (default "localhost:8884")
      --oauth-server-address string                     OAuth Server address (default "https://localhost/oauth")
      --output-format string                            Output format (default "json")
      --packet-broker-agent-grpc-address string         Packet Broker Agent address (default "localhost:8884")
      --qr-code-generator-grpc-address string           QR Code Generator address (default "localhost:8884")
      --retry-config.default-timeout duration           Default timeout between retry attempts (default 100ms)
      --retry-config.enable-metadata                    Use request response metadata to dynamically calculate timeout between retry attempts (default true)
      --retry-config.jitter float                       Fraction that creates a deviation of the timeout used between retry attempts
      --retry-config.max uint                           Maximum amount of times that a request can be reattempted
      --skip-version-check                              Do not perform version checks
```

### SEE ALSO

* [ttn-lw-cli gateways]({{< relref "ttn-lw-cli_gateways" >}})	 - Gateway commands
* [ttn-lw-cli gateways claim authorize]({{< relref "ttn-lw-cli_gateways_claim_authorize" >}})	 - Authorize an gateway for claiming (EXPERIMENTAL)
* [ttn-lw-cli gateways claim unauthorize]({{< relref "ttn-lw-cli_gateways_claim_unauthorize" >}})	 - Unauthorize an gateway for claiming (EXPERIMENTAL)
