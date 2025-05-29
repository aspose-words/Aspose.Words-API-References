---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Seriendruckprozess mit der Eigenschaft „MergeDuplicateRegions“. Steuern Sie, wie Datenquellenbereiche zusammengeführt werden, für ein effizientes Dokumentenmanagement.
type: docs
weight: 60
url: /de/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob beim Ausführen eines Seriendrucks mit Regionen für die Datenquelle alle Seriendruckregionen des Dokuments mit dem Namen einer Datenquelle oder nur die erste zusammengeführt werden sollen.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt, wie mit doppelten Seriendruckbereichen gearbeitet wird.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Wenn wir die Eigenschaft "MergeDuplicateRegions" auf "false" setzen, betrifft der Serienbrief die erste Region,
    // während die MERGEFIELDs des zweiten im Zustand vor dem Zusammenführen verbleiben.
    // Um beide Regionen auf diese Weise zusammenzuführen,
    // wir müssten den Serienbrief zweimal auf einer Tabelle mit demselben Namen ausführen.
    // Wenn wir die Eigenschaft „MergeDuplicateRegions“ auf „true“ setzen, wirkt sich der Serienbrief auf beide Regionen aus.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Gibt ein Dokument zurück, das zwei doppelte Serienbriefbereiche enthält (mit demselben Namen in den Tags „TableStart/End“).
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

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
