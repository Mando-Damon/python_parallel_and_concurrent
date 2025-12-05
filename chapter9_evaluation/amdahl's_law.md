# Amdahl's Law    
# 阿姆达尔定律  
  
Amdahl's Law is an equation used to estimate the potential speedup of a parallel program.    
阿姆达尔定律是一种用于估算并行程序潜在加速比的公式。  
  
It helps determine the effectiveness of parallelizing a program based on its parallelizable portion.    
它帮助我们根据程序中可并行化部分的比例，判断并行化的效果。  
  
---  
  
## The Equation    
## 公式  
  
Overall Speedup = 1 / [ (1 - P) + (P / S) ]  
  
- **P**: The fraction of the program that can be parallelized    
  **P**：程序中可并行化的部分比例  
- **S**: The speedup for the parallelized part (often equals number of processors)    
  **S**：并行部分的加速比（通常等于处理器数量）  
  
---  
  
## Example    
## 示例  
  
Barron uses a program with 95% parallelizable code as an example:    
Barron 用一个95%可并行化代码的程序举例：  
  
- With **2 processors**, overall speedup ≈ 1.9    
  2个处理器时，总加速比约为1.9  
- With **3 processors**, speedup ≈ 2.7    
  3个处理器时，加速比约为2.7  
- With **4 processors**, speedup ≈ 3.5    
  4个处理器时，加速比约为3.5  
- Even with **1000 processors**, max speedup ≈ 19.6    
  即使有1000个处理器，最大加速比也只有约19.6  
- With **1,000,000 processors**, speedup is just under 20    
  一百万处理器时，加速比也不到20  
  
The non-parallelizable 5% of the program creates an upper limit on achievable speedup.    
程序中不可并行的5%部分限制了最大加速比。  
  
---  
  
## Limitations on Effectiveness    
## 并