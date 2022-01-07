This paper introduces a graph-based way to represent data flow analysis and do some compiler optimizations through machine learning.  
PROGRAML, what the researchers invented, is a novel IR-based program representation. This representation is similar to the data structures used typically in inter-procedural data flow analysis, but it can be processed natively by deep learning models. The programl graph can be crafted by traversaling a compiler IR. An empty graph G = 0 is made up with three stages: control-flow, data-flow, and call-flow. The graph in control-flow stage consist of the vertexes that represent each instruction in IR scripts. In addition, the directed edges between vertexes are means the executing orders. The second stage, data-flow stage, add the vertexes representing the constants and variables, and the edges representing use and defination relations. The in-edge for a data vertex means define a data to the variable, while the out-edge means that a instruction uses this data. The third stage is the call flow. This stage is adding the call edges that capture the relation between an instruction that call a function and enty instruction of the called function. Moreover, the return call edge are added from the terminal statement of an function to the call instruction. The different stages are showed below.
![[Pasted image 20220101100520.png]]
The Program to IR represent
![[Pasted image 20220101100530.png]]
The first Stage - Control flow
![[Pasted image 20220101100614.png]]
The Second Stage - Data Flow
![[Pasted image 20220101100629.png]]
The Third Stage - Call Flow

