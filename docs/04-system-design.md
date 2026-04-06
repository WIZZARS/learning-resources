# System Design & Architecture

## Architecture Patterns

### Monolithic Architecture
- Single codebase, all features together
- **Pros**: Simpler to develop initially, easier deployment
- **Cons**: Hard to scale, technology lock-in, difficult to maintain at scale

### Microservices Architecture
- Multiple independent services, each with own database
- **Pros**: Easy to scale, independent deployment, technology flexibility
- **Cons**: Complex, distributed system challenges, network latency
- **Communication**: REST, gRPC, Message Queues

### Layered Architecture
```
└─ Presentation Layer (UI, API)
   └─ Business Logic Layer (Services, validations)
      └─ Persistence Layer (Database, ORM)
         └─ Database
```

### Event-Driven Architecture
- Components communicate through events
- Producer emits event, consumers react
- **Tools**: Kafka, RabbitMQ, AWS SNS/SQS

## Design Patterns

### Creational Patterns (Object Creation)

#### Singleton
- Only one instance of class exists
- Use for: Logger, Database connection, Config manager

#### Factory
- Creates objects without exposing creation logic
- Use for: Creating different types of objects

#### Builder
- Creates complex objects step by step
- Use for: Objects with many optional parameters

### Structural Patterns (Object Composition)

#### Adapter
- Makes incompatible interfaces compatible
- Use for: Integration with legacy code

#### Decorator
- Adds new functionality to objects dynamically
- Use for: Adding features without modifying original class

#### Facade
- Provides simplified interface to complex subsystem
- Use for: Simplifying library usage

### Behavioral Patterns (Object Interaction)

#### Observer
- Notifies multiple objects about state changes
- Use for: Event handling, pub-sub systems

#### Strategy
- Encapsulates different algorithms
- Use for: Sort algorithms, payment methods

#### Command
- Encapsulates request as an object
- Use for: Undo/redo, queuing operations

## Caching Strategies

### Cache Types
- **In-Memory**: Redis, Memcached (fast, limited size)
- **Database**: Query result caching
- **HTTP**: Browser cache, CDN

### Cache Invalidation
- **Time-based (TTL)**: Expire after X seconds
- **Event-based**: Invalidate on specific events
- **LRU**: Least Recently Used eviction
- **Write-through**: Update cache and DB simultaneously
- **Write-behind**: Update cache first, DB later

## Load Balancing

### Strategies
- **Round Robin**: Distribute evenly
- **Least Connections**: Route to least busy server
- **IP Hash**: Same client always goes to same server
- **Resource-based**: Based on server CPU/memory

### Tools
- Nginx, HAProxy, AWS ELB, Google Cloud Load Balancer

## Database Scaling

### Vertical Scaling
- Upgrade single server (more CPU, RAM)
- Easier but has limits

### Horizontal Scaling
- Add more servers
- **Sharding**: Partition data by key
- **Replication**: Master-Slave setup
- **Read Replicas**: Handle read-heavy workloads

## Rate Limiting

### Algorithms
- **Token Bucket**: Tokens refill at fixed rate
- **Sliding Window**: Track requests in time window
- **Leaky Bucket**: Constant outflow rate

### Implementation
- Per IP address
- Per user/API key
- Per endpoint

## Monitoring & Observability

### The Three Pillars

#### Logging
- Record events and errors
- Structured logging (JSON format)
- Log levels: DEBUG, INFO, WARN, ERROR

#### Metrics
- Quantitative measurements
- Types: Counter, Gauge, Histogram
- Examples: Request count, Response time, Error rate

#### Tracing
- Track request flow through system
- Identify bottlenecks
- Tools: Jaeger, Zipkin, Datadog

### Key Metrics
- **Response Time**: How long requests take
- **Error Rate**: Percentage of failed requests
- **Throughput**: Requests processed per second
- **Availability**: System uptime percentage
- **Resource Usage**: CPU, Memory, Disk, Network

## Reliability Concepts

### Redundancy
- Avoid single points of failure
- Replicate critical components

### Circuit Breaker
- Prevent cascading failures
- States: Closed (normal), Open (failing), Half-open (recovering)

### Retry Logic
- Exponential backoff: Wait longer between retries
- Don't retry: 4xx errors (client fault)
- Retry: 5xx errors, network timeouts

### Graceful Degradation
- Degrade functionality when components fail
- Show cached data if DB is down

---
**Last Updated**: 2026-04-05
