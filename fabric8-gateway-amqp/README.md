# fabric8-gateway-amqp
This should be deployed onto a Fabric8 node running the Gateway MQ profile.

## What does it do?
Sends a simple AMQP message and attempts it read it.

## How to use it?
Set loadbalancer to:

- Type: GET
- URL: http://{gateway-ip}:9200/amqp-healthcheck
- Response: HTTPCode == 200 && BodyContent == true

### Install into Fuse
features:addurl mvn:com.garethahealy.loadbalancer-healthchecks/fabric8-gateway-amqp/1.0.1-SNAPSHOT/xml/features
features:install fabric8-gateway-amqp
