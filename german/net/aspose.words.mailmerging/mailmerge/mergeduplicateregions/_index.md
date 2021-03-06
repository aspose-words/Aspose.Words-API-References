---
title: MergeDuplicateRegions
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft oder setzt einen Wert der angibt ob alle Dokument-Seriendruckregionen mit dem Namen einer Datenquelle zusammengeführt werden sollen wenn ein Seriendruck mit Regionen gegen die Datenquelle ausgeführt wird oder nur der erste.
type: docs
weight: 60
url: /de/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Ruft oder setzt einen Wert, der angibt, ob alle Dokument-Seriendruckregionen mit dem Namen einer Datenquelle zusammengeführt werden sollen, wenn ein Seriendruck mit Regionen gegen die Datenquelle ausgeführt wird, oder nur der erste.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

### Bemerkungen

Der Standardwert ist **FALSCH** .

### Beispiele

Zeigt, wie mit doppelten Seriendruckbereichen gearbeitet wird.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Wenn wir die Eigenschaft "MergeDuplicateRegions" auf "false" setzen, wirkt sich der Seriendruck auf die erste Region aus,
    // während die MERGEFIELDs des zweiten im Pre-Merge-Zustand belassen werden.
    // Um beide Regionen so zusammenzuführen,
    // wir müssten den Seriendruck zweimal auf einer gleichnamigen Tabelle ausführen.
    // Wenn wir die Eigenschaft "MergeDuplicateRegions" auf "true" setzen, wirkt sich der Seriendruck auf beide Regionen aus.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Gibt ein Dokument zurück, das zwei doppelte Seriendruckbereiche enthält (die denselben Namen in den "TableStart/End"-Tags haben).
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Erstellt eine Datentabelle mit einer Zeile und zwei Spalten.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Siehe auch

* class [MailMerge](../../mailmerge)
* namensraum [Aspose.Words.MailMerging](../../mailmerge)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
