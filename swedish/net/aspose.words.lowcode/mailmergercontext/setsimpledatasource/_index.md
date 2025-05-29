---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words för .NET
description: Förbättra effektiviteten i din dokumentkoppling med MailMergerContext SetSimpleDataSource-metoden, vilket effektiviserar konfigurationen av datakällor för sömlös exekvering.
type: docs
weight: 40
url: /sv/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Anger datakällan som används för att utföra enkel dokumentkoppling.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Anmärkningar

Om både datakällan för enkel dokumentkoppling och datakällan för dokumentkoppling med regioner anges, körs först dokumentkoppling med regioner och sedan körs enkel dokumentkoppling.

## Exempel

Visar hur man utför en dokumentkopplingsoperation för en enskild post med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkoppling:
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

Visar hur man utför en dokumentkopplingsåtgärd för en enskild post från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkoppling med hjälp av dokument från strömmen:
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

### Se även

* class [MailMergerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Anger datakällan som används för att utföra enkel dokumentkoppling.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Anmärkningar

Om både datakällan för enkel dokumentkoppling och datakällan för dokumentkoppling med regioner anges, körs först dokumentkoppling med regioner och sedan körs enkel dokumentkoppling.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en DataRow med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en koppling mellan dokument från en DataRow:
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

Visar hur man utför en dokumentkopplingsoperation från en DataRow med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en DataRow med hjälp av dokument från strömmen:
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

### Se även

* class [MailMergerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Anger datakällan som används för att utföra enkel dokumentkoppling.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Anmärkningar

Om både datakällan för enkel dokumentkoppling och datakällan för dokumentkoppling med regioner anges, körs först dokumentkoppling med regioner och sedan körs enkel dokumentkoppling.

## Exempel

Visar hur man utför en dokumentkopplingsoperation från en datatabell med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell:
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

Visar hur man utför en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen:
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

### Se även

* class [MailMergerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
