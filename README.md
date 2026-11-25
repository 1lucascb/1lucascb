# Hey, I'm Lucas 👋

I'm a **Back-End Software Engineer** focused on building reliable, scalable systems and understanding the engineering principles behind them.

My primary technologies are **Python, Go, and Java**. I've worked across backend architecture, API development, distributed systems, databases, messaging, cloud infrastructure, and AI-powered applications.

My main interests include **system design, distributed systems, performance engineering, cloud infrastructure, and LLM-based systems**.

I also write about things I learn and build, particularly around AI agents and LLM-powered architectures, on my [personal website](https://ptfl.lcb936.com/).

<!-- CUSTOM_CONTENT_START -->
---
**☕ Daily Engineering Digest - 2026-11-25** · `Engineering Concept`

### Backpressure in Message-Processing Systems

Backpressure is a flow-control mechanism where a downstream consumer signals an upstream producer to slow down or pause when it cannot process data at the current rate. This prevents buffer overflow, memory exhaustion, and cascading failures in distributed pipelines.

**Practical Example**
In a Kafka-based architecture, if a consumer service (e.g., a database writer) becomes slower than the producer, the consumer's fetch offset lags. Instead of pulling unbounded messages into local memory, the consumer stops fetching new batches. The broker retains the data, and the producer may eventually hit its own limits if the consumer remains stalled.

**Trade-offs**
| Strategy | Benefit | Risk |
| :--- | :--- | :--- |
| **Bounded Buffers** | Predictable memory usage | Potential message rejection or head-of-line blocking |
| **Rate Limiting** | Smooths out bursts | Increased end-to-end latency |

**Technical Takeaway**
Implementing explicit backpressure requires designing APIs that propagate load signals. For example, in Go, use buffered channels with non-blocking sends (`select` with `default`) to drop or queue requests gracefully rather than blocking the caller indefinitely. In Python, leverage `asyncio.Queue` with a max size to trigger `await put()` only when space is available, ensuring the producer awaits the consumer's capacity.
<!-- CUSTOM_CONTENT_END -->
