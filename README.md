# Awesome-Event-Bus-Pub-Sub-Messaging

# Top Event Bus Pub/Sub Messaging Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Event Streaming, Message Brokers & Real-Time Delivery*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Event Bus & Pub/Sub Messaging**. These tools enable organizations to build event-driven architectures, decouple microservices, stream data in real-time, and deliver messages reliably across distributed systems.

**Examples** include Salesforce Event Bus, Apache Kafka, AWS EventBridge, Google Cloud Pub/Sub, Azure Event Grid, RabbitMQ Cloud, Solace PubSub+, Ably, Pusher Channels, and Redpanda Cloud (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom messaging infrastructure, and open event streaming — ideal for platform engineers, architects, and developers seeking transparent, vendor-independent pub/sub messaging.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Salesforce Event Bus](https://developer.salesforce.com/docs/platform/pub-sub-api/guide/expanded-event-bus.html)**
  Multitenant, multicloud event storage and delivery service based on publish-subscribe model. Time-ordered event log stores messages for 72 hours, ensuring ordered delivery. Features Pub/Sub API (gRPC/HTTP2, Apache Avro) for publishing and subscribing to platform events and change data capture events. Replay ID enables stream recovery after specific event IDs. Expanded service built outside main CRM stack for cross-cloud integration between Sales Cloud, Service Cloud, Marketing Cloud, Commerce Cloud, and Tableau Analytics . Event Relay provides no-code delivery to Amazon EventBridge .

- **[Apache Kafka](https://kafka.apache.org/)**
  Industry-standard distributed event streaming platform. Features high-throughput, fault-tolerant, durable log-based messaging. Massive ecosystem including Kafka Connect, Kafka Streams, and ksqlDB.

- **[AWS EventBridge](https://aws.amazon.com/eventbridge/)**
  Serverless event bus service for routing events between AWS services, SaaS applications, and custom applications. Features event rules, schema registry, and partner event sources including Salesforce .

- **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)**
  Fully managed, scalable messaging service. Features at-least-once delivery, global message ordering, push/pull subscriptions, and dead-letter topics.

- **[Azure Event Grid](https://azure.microsoft.com/en-us/products/event-grid/)**
  Fully managed event routing service. Features built-in support for Azure services, custom topics, and partner event sources.

- **[RabbitMQ Cloud](https://www.rabbitmq.com/)**
  Managed RabbitMQ service. Features AMQP, MQTT, STOMP protocols with flexible routing, message queuing, and pub/sub capabilities.

- **[Solace PubSub+](https://solace.com/)**
  Enterprise event broker supporting multiple open standard protocols (AMQP, MQTT, JMS, REST) and message exchange patterns. Features dynamic message routing, high availability with 1:1 broker pairing, disaster recovery without external mechanisms, and slow consumer handling that doesn't impact publishers . Deployable in any PaaS environment including Kubernetes, VMWare Tanzu, Red Hat OpenShift, and SAP Cloud .

- **[Ably](https://ably.com/)**
  Real-time messaging platform with pub/sub channels. Features global edge network, guaranteed delivery, and presence capabilities.

- **[Pusher Channels](https://pusher.com/)**
  Hosted pub/sub messaging service. Features WebSocket-based real-time communication with channels, presence, and webhooks.

- **[Redpanda Cloud](https://www.redpanda.com/redpanda-cloud)**
  Fully managed streaming data platform with Kafka API compatibility. Built on same high-performance core without JVM or ZooKeeper. Features BYOC (Bring Your Own Cloud) for data sovereignty, Dedicated clusters on Redpanda infrastructure, and Serverless clusters with zero base cost. 99.9% uptime SLA for Serverless, 99.99% for BYOC. Runs on 3x fewer compute resources than Apache Kafka, with tiered storage delivering 8-9x savings in long-term retention costs .

## Open-Source GitHub Projects

- **[Centrifugo](https://github.com/centrifugal/centrifugo)**
  Scalable real-time messaging server in a language-agnostic way (Apache-2.0). Self-hosted alternative to Pubnub, Pusher, Ably, socket.io, Phoenix.PubSub, and SignalR. 11k+ GitHub stars . Features efficient real-time transports (WebSocket, HTTP-streaming, SSE, GRPC, WebTransport), built-in scalability with Redis or Nats, simple HTTP/GRPC server API, asynchronous PostgreSQL and Kafka consumers for transactional outbox and CDC patterns, JWT and proxy authentication, channel subscription multiplexing, hot message history with automatic recovery, delta compression, presence information, and embedded admin web UI .

- **[Outpost (Hookdeck)](https://github.com/hookdeck/outpost)**
  Self-hostable open-source outbound webhooks and event destinations infrastructure (Apache-2.0). Built for SaaS and API platforms that need to push events to customer-defined destinations including webhook endpoints, message queues (SQS, RabbitMQ, Kinesis), and event buses . Features at-least-once delivery with retry logic and exponential backoff, multi-tenant support, REST API for publishing events, SDKs for Go/TypeScript/Python, developer portal with delivery logs, topic-based subscriptions, OpenTelemetry integration, and destination auto-disable on failure .

- **[Ripple](https://github.com/madisoheib/Ripple)**
  Self-hosted, Pusher-compatible WebSocket server (license varies) — a single static Rust binary. Speaks Pusher Channels protocol so existing clients work unchanged (Laravel Echo, pusher-js, pusher-php-server, mobile SDKs). No Redis, Node, or PHP extensions required. Features bounded buffers with slow-client disconnect, all cores native Rust concurrency. Benchmarks show 512 MiB at 40k connections vs Reverb's 834 MiB, sustained 50k deliveries/s at p50 14.7ms vs Reverb's 24.6ms, and CPU at ~13% vs Reverb's 62% .

- **[Soketi](https://github.com/soketi/soketi)**
  Next-gen, Pusher-compatible, open-source WebSocket server (MIT). Implements Pusher protocol so existing Pusher SDKs and applications can drop-in replace Pusher Channels with self-hosted Soketi. Written in Node/TypeScript with Rust adapter. Features public, private, presence, and encrypted channels. Horizontal scaling via Redis adapter. Deployable via npm, Docker, Kubernetes, or systemd .

- **[Event (rbaliyan)](https://github.com/rbaliyan/event)**
  Go event bus library (license varies) with reliability primitives for production event-driven systems . Features outbox pattern for transactional publishing, idempotency middleware, poison message detection with quarantine, per-message monitoring state, schema provider with strict mode, dead letter queue with retry limits, producer-side audit log, graceful drain timeout, and subscriber timeout handling. Supports Redis Streams (recommended for production) and NATS transports with consumer groups for at-least-once delivery .

### Additional Strong Open-Source Options

- **[NATS](https://github.com/nats-io/nats-server)** — Cloud-native messaging system (Apache-2.0) with pub/sub, request/reply, and JetStream persistence.
- **[RabbitMQ](https://github.com/rabbitmq/rabbitmq-server)** — Open-source message broker (MPL-2.0) with AMQP, MQTT, and STOMP support.
- **[Redis Streams](https://github.com/redis/redis)** — Log-based messaging with consumer groups and at-least-once delivery.
- **[Apache Pulsar](https://github.com/apache/pulsar)** — Distributed pub/sub messaging with multi-tenancy and geo-replication.
- **[EMQX](https://github.com/emqx/emqx)** — MQTT broker (Apache-2.0) for IoT and real-time messaging at scale.
- **[MQTT.js](https://github.com/mqttjs/MQTT.js)** — MQTT client for JavaScript/Node.js pub/sub applications.
- Community **n8n** workflows for event routing and cross-platform message delivery.

**Frameworks for building custom systems**: Combine **Centrifugo** or **Ripple** for real-time WebSocket delivery with **NATS** or **RabbitMQ** for reliable message brokering, **Outpost** for outbound webhook infrastructure, **Event (rbaliyan)** for reliability primitives (outbox, DLQ, idempotency), and **PostgreSQL** for persistence — creating a fully self-hosted, enterprise-grade pub/sub messaging platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Event bus and messaging systems handling business events must comply with data protection regulations (GDPR, CCPA, etc.).
- Self-hosted open-source solutions require proper security hardening, TLS configuration, and ongoing maintenance. Message delivery guarantees (at-least-once, exactly-once) have different trade-offs—choose based on idempotency requirements and downstream tolerance for duplicates.

---

**Made for platform engineers, architects, backend developers, and organizations building transparent event-driven solutions.**  
Let's make Event Bus & Pub/Sub Messaging more open, data-driven, and reliable.
