
```vb.net
ReportTable.AsEnumerable().Any(Function(x) x("Call ID").ToString.Trim.Equals(row("itemId").ToString.trim))

If(ClaimSubmitTypeDt.AsEnumerable.Any(function(r) r("Provider Code").ToString.Trim.Equals("22889")),"I","D")

```