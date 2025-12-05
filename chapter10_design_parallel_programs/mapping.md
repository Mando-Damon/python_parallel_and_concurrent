# Mapping in Parallel Design    
# 并行设计中的映射  
  
---  
  
## What is Mapping?    
什么是映射？  
  
- Mapping is the fourth and final stage in the parallel design process.  
- 它涉及为每个已建立的任务指定在哪个处理器上执行。  
- 在单处理器或自动任务调度的系统中不需要映射；在分布式系统或专用硬件（如并行处理器）下则非常重要。  
  
---  
  
## When is Mapping Needed?    
## 何时需要映射？  
  
- **Not needed:** 单处理器系统、自动任务调度系统（如某些多核 CPU）。  
- **Needed:** 分布式系统、多处理器并行硬件、GPU 等。  
  
---  
  
## Goals and Strategies    
## 目标与策略  
  
**主要目标：**    
- 最小化总执行时间  
  
**关键策略：**    
1. **Increasing concurrency**    
   提高并发性    
   - 将可并行执行的任务分配到不同处理器上  
  
2. **Improving locality**    
   提高局部性    
   - 将频繁通信的任务分配在同一个处理器上，使其“靠近”，减少通信延迟  
  
---  
  
## Challenges and Considerations    
## 挑战与考虑因素  
  
- 上述策略常常互相冲突，需要设计上的权衡  
  - 并发性高可能导致通信成本增加  
  - 增强局部性可能降低并发性  
  
- 动态任务负载可能需要周期性重新映射（动态负载均衡）  
  
- 映射算法的设计高度依赖于程序结构和硬件规格  
  
- 许多负载均衡算法结合了域分解和聚合技术  
  
---  
  
你可以复制此 Markdown 用于中英文学习或笔记。  