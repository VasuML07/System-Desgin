# 🚦 Rate Limiting – System Design Mastery Guide

Rate limiting protects systems from overload.

Without rate limiting:
- APIs can be abused
- Servers can crash
- Resources can be exhausted

Rate limiting ensures:
- Fair usage
- System stability
- Abuse prevention
- Predictable performance

---

# 🎯 Core Concepts to Master

## 1️⃣ Why Rate Limiting?

- Prevent DDoS attacks
- Avoid server overload
- Enforce API usage tiers
- Protect backend services

Example:
Allow 100 requests per minute per user.

---

## 2️⃣ Common Algorithms

### Fixed Window Counter
- Simple
- Resets every fixed interval
- Can cause burst at boundary

### Sliding Window Log
- Stores timestamps
- More accurate
- Higher memory usage

### Sliding Window Counter
- Approximate
- Better balance between accuracy & memory

### Token Bucket
- Tokens added at fixed rate
- Allows bursts
- Very popular in production

### Leaky Bucket
- Constant outflow rate
- Smooth traffic

Understand trade-offs clearly.

---

## 3️⃣ Distributed Rate Limiting

Challenges:
- Multiple servers
- Shared counters
- Synchronization

Solutions:
- Redis-based centralized store
- Consistent hashing
- Sharding counters

---

## 4️⃣ Where to Apply Rate Limiting?

- API Gateway
- Load Balancer level
- Application level
- Reverse proxy (Nginx)

---

## 5️⃣ Key Design Considerations

- Per-user vs global limits
- IP-based limits
- Authenticated vs unauthenticated users
- Fail-open vs fail-closed behavior

---

# 📚 Learning Resources

## 📘 Official & High-Quality Guides

### 1️⃣ AWS API Gateway Rate Limiting
https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html

### 2️⃣ Cloudflare Rate Limiting Overview
https://developers.cloudflare.com/waf/rate-limiting-rules/

### 3️⃣ System Design Primer – Rate Limiting Section
https://github.com/donnemartin/system-design-primer#rate-limiting

---

## 🎥 YouTube (High Quality)

### 4️⃣ Hussein Nasser – Rate Limiting Deep Dive
https://www.youtube.com/c/HusseinNasser-software-engineering

### 5️⃣ ByteByteGo – Token Bucket Explained
https://www.youtube.com/c/ByteByteGo

---

# 🧠 Practice Problems

Rate limiting is tested indirectly through:
- Design problems
- Sliding window logic
- Time-based data structures
- Concurrency

Platforms included:
- LeetCode
- CodeStudio (Coding Ninjas)
- GeeksforGeeks

---

# 🔹 LeetCode

1. Design Hit Counter  
https://leetcode.com/problems/design-hit-counter/

2. Logger Rate Limiter  
https://leetcode.com/problems/logger-rate-limiter/

3. Time Based Key-Value Store  
https://leetcode.com/problems/time-based-key-value-store/

4. Sliding Window Maximum  
https://leetcode.com/problems/sliding-window-maximum/

5. Number of Recent Calls  
https://leetcode.com/problems/number-of-recent-calls/

6. Find Servers That Handled Most Number of Requests  
https://leetcode.com/problems/find-servers-that-handled-most-number-of-requests/

---

# 🔹 CodeStudio (Coding Ninjas)

1. Design Rate Limiter  
https://www.codingninjas.com/studio/problems/design-a-rate-limiter_1170056

2. Sliding Window Problems  
https://www.codingninjas.com/studio/problems/sliding-window_1170045

3. Producer Consumer Problem  
https://www.codingninjas.com/studio/problems/producer-consumer_1170057

---

# 🔹 GeeksforGeeks

1. Token Bucket Algorithm  
https://www.geeksforgeeks.org/token-bucket-algorithm/

2. Leaky Bucket Algorithm  
https://www.geeksforgeeks.org/leaky-bucket-algorithm/

3. Rate Limiting in Distributed Systems  
https://www.geeksforgeeks.org/rate-limiting-in-distributed-system/

---

# 🚀 Mini Projects to Build

To deeply understand rate limiting:

- Implement fixed window limiter in memory
- Build token bucket limiter using Redis
- Add per-user API limits
- Add global request cap
- Simulate traffic spikes
- Integrate limiter into backend API

Optional:
Deploy and test under load.

---

# 🏁 Final Goal

After mastering rate limiting, you should be able to:

- Explain algorithm trade-offs
- Implement sliding window logic
- Design distributed rate limiting
- Protect APIs from abuse
- Handle burst traffic safely

Rate limiting is not just throttling.
It is traffic discipline.

If load balancing distributes traffic,
rate limiting controls it.

Master this, and your system design answers become production-aware.
