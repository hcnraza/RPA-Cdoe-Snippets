## To check the Value exist in Dt
```Linq
ReportTable.AsEnumerable().Any(Function(x) x("Call ID").ToString.Trim.Equals(row("itemId").ToString.trim))
```
```Linq
If(ClaimSubmitTypeDt.AsEnumerable.Any(function(r) r("Provider Code").ToString.Trim.Equals("22889")),"I","D")
```
