## For example we have one variable type int NextAgentRowIndex
## rowIndex+1 is our counter variable which is starting from 0
```linq
NextAgentRowIndex = rowIndex+1
NextAgentRowIndex = If(NextAgentRowIndex >= AgentDT.Rows.Count,0,NextAgentRowIndex)
IF(Condition , Then , Else)
```
### We can use writeline to display 
```linq
AgentDT.Rows(NextAgentRowIndex).item("Agent Name").ToString
```
### Here we do not need to go for For each we can use Linq for this
