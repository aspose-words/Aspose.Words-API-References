---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der MailMerge-Eigenschaft UseWholeParagraphAsRegion Ihre Serienbriefbereiche verbessern und so die vollständige Kontrolle über die Inhaltseinbindung gewährleisten.
type: docs
weight: 160
url: /de/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Ruft einen Wert ab oder setzt ihn, der angibt, ob der ganze Absatz mit**TischStart** oder**Tabellenende** field oder bestimmter Bereich zwischen**TischStart** Und**Tabellenende** Felder sollten in den Serienbriefbereich aufgenommen werden.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

## Beispiele

Zeigt die Beziehung zwischen Seriendruckbereichen und Absätzen.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // Standardmäßig kann ein Absatz zu nicht mehr als einem Seriendruckbereich gehören.
    // Der Inhalt unseres Dokuments erfüllt diese Kriterien nicht.
    // Wenn wir das Flag "UseWholeParagraphAsRegion" auf "true" setzen,
    // Das Ausführen eines Serienbriefs für dieses Dokument löst eine Ausnahme aus.
    // Wenn wir das Flag "UseWholeParagraphAsRegion" auf "false" setzen,
    // Wir können für dieses Dokument einen Serienbrief ausführen.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // Der Serienbrief füllt unsere erste Region, während die zweite Region ungenutzt bleibt
    // da es die Region ist, die die Regel bricht.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Erstellen Sie ein Dokument mit zwei Serienbriefbereichen, die sich einen Absatz teilen.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// Erstellen Sie eine Datentabelle, die während eines Serienbriefs eine Region füllen kann.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
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
