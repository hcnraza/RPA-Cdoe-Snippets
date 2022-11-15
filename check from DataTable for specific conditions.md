```linq
AgentsDT.AsEnumerable().Where(function(x) x("Attendance").ToString="Yes" And DateTime.Now > Convert.ToDateTime(x("start time")) And DateTime.Now<Convert.ToDateTime(x("end time"))) .CopyToDataTable
```
