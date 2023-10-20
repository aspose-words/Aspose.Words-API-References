---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words für .NET
description: MailMerge MergeDuplicateRegions eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob alle DokumentSeriendruckbereiche mit dem Namen einer Datenquelle beim Ausführen eines Seriendrucks mit Bereichen für die Datenquelle zusammengeführt werden sollen oder nur der erste in C#.
type: docs
weight: 60
url: /de/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob alle Dokument-Seriendruckbereiche mit dem Namen einer Datenquelle beim Ausführen eines Seriendrucks mit Bereichen für die Datenquelle zusammengeführt werden sollen oder nur der erste.

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

    // Wenn wir die Eigenschaft „MergeDuplicateRegions“ auf „false“ setzen, wirkt sich der Seriendruck auf die erste Region aus.
    // während die MERGEFIELDs des zweiten im Zustand vor der Zusammenführung belassen werden.
    // Um beide Regionen auf diese Weise zusammenzuführen,
    // wir müssten den Serienbrief zweimal für eine Tabelle mit demselben Namen ausführen.
    // Wenn wir die Eigenschaft „MergeDuplicateRegions“ auf „true“ setzen, wirkt sich der Seriendruck auf beide Regionen aus.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Gibt ein Dokument zurück, das zwei doppelte Seriendruckbereiche enthält (mit demselben Namen in den „TableStart/End“-Tags).
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
