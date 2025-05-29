---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die MailMerge-Eigenschaft „MergeWholeDocument“ alle Felder während eines regionsbasierten Seriendrucks aktualisiert und so die Effizienz und Genauigkeit Ihrer Dokumente verbessert.
type: docs
weight: 70
url: /de/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Seriendrucks mit Regionen aktualisiert werden.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt die Beziehung zwischen Serienbriefen mit Regionen und Feldaktualisierungen.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Wenn wir das Flag "MergeWholeDocument" auf "true" setzen,
    // Der Serienbrief mit Regionen aktualisiert jedes Feld im Dokument.
    // Wenn wir das Flag "MergeWholeDocument" auf "false" setzen, aktualisiert der Serienbrief nur die Felder
    // innerhalb des Serienbriefbereichs, dessen Name mit dem Namen der Datenquellentabelle übereinstimmt.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Der Serienbrief aktualisiert nur das Feld QUOTE außerhalb des Serienbriefbereichs
    // wenn wir das Flag „MergeWholeDocument“ auf „true“ setzen.
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Erstellen Sie ein Dokument mit einem Seriendruckbereich, der zu einer Datenquelle mit dem Namen „MyTable“ gehört.
/// Fügen Sie innerhalb dieses Bereichs ein QUOTE-Feld und außerhalb ein weiteres ein.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Erstellen Sie eine Datentabelle, die in einem Serienbrief verwendet wird.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
