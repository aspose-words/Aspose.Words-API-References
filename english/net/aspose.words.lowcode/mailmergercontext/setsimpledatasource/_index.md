---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words for .NET
description: Enhance your mail merge efficiency with the MailMergerContext SetSimpleDataSource method, streamlining data source setup for seamless execution.
type: docs
weight: 40
url: /net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Sets data source used to execute simple mail merge.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Remarks

If both simple mail merge data source and data source for mail merge with regions are specified, mail merge with regions is executed first and then simple mail merge is executed.

## Examples

Shows how to do mail merge operation for a single record using context.

```csharp
// There is a several ways to do mail merge operation:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Shows how to do mail merge operation for a single record from the stream using context.

```csharp
// There is a several ways to do mail merge operation using documents from the stream:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### See Also

* class [MailMergerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Sets data source used to execute simple mail merge.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Remarks

If both simple mail merge data source and data source for mail merge with regions are specified, mail merge with regions is executed first and then simple mail merge is executed.

## Examples

Shows how to do mail merge operation from a DataRow using context.

```csharp
// There is a several ways to do mail merge operation from a DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataRow);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataRow.docx")
    .Execute();
```

Shows how to do mail merge operation from a DataRow using documents from the stream using context.

```csharp
// There is a several ways to do mail merge operation from a DataRow using documents from the stream:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataRow);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataRow.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### See Also

* class [MailMergerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Sets data source used to execute simple mail merge.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Remarks

If both simple mail merge data source and data source for mail merge with regions are specified, mail merge with regions is executed first and then simple mail merge is executed.

## Examples

Shows how to do mail merge operation from a DataTable using context.

```csharp
// There is a several ways to do mail merge operation from a DataTable:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataTable.docx")
    .Execute();
```

Shows how to do mail merge operation from a DataTable using documents from the stream using context.

```csharp
// There is a several ways to do mail merge operation from a DataTable using documents from the stream:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### See Also

* class [MailMergerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
