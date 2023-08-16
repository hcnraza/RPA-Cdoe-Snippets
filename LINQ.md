# Create Dataset using Unique Column

```vb.net

' Grouping and filtering rows using LINQ
Dim groupedData = From row In DT_WorkItems.AsEnumerable()
	Let email = row.Field(Of String)("Agent Email")
	Where String.IsNullOrEmpty(email).Equals(False)
	Group row By email Into Group
	Select New With {
		.Email = email,
		.Rows = Group.CopyToDataTable()
		}							}
'Creating a dataset and adding tables for each group
Dim dataSet As New DataSet()	
		For Each Group In groupedData
			Dim datatable = Group.Rows
			datatable.TableName= Group.Email '  Make it Agent Name
			dataSet.Tables.Add(datatable)
		Next
out_AgentDataSet =dataSet.Copy		
```
