---
title: MailMerge.PreserveUnusedTags
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob die nicht verwendeten MustacheTags beibehalten werden sollen.
type: docs
weight: 80
url: /de/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob die nicht verwendeten „Mustache“-Tags beibehalten werden sollen.

```csharp
public bool PreserveUnusedTags { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH` .

### Beispiele

Zeigt, wie das Erscheinungsbild alternativer Seriendruck-Tags erhalten bleibt, die während eines Seriendrucks nicht verwendet werden.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Standardmäßig platziert ein Serienbrief Daten aus jeder Zeile einer Tabelle in MERGEFIELDs, die Spalten in dieser Tabelle benennen.
    // Unser Dokument hat keine solchen Felder, aber Klartext-Tags, die in geschweifte Klammern eingeschlossen sind.
    // Wenn wir das Flag „PreserveUnusedTags“ auf „true“ setzen, könnten wir diese Tags als MERGEFIELDs behandeln
    // damit unser Serienbrief an diesen Tags Daten aus der Datenquelle einfügen kann.
    // Wenn wir das Flag „PreserveUnusedTags“ auf „false“ setzen,
    // Der Seriendruck wandelt diese Tags in MERGEFIELDs um und lässt sie leer.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Unser Dokument hat ein Tag für eine Spalte namens „Column2“, die in der Tabelle nicht vorhanden ist.
    // Wenn wir das Flag „PreserveUnusedTags“ auf „false“ setzen, then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Erstellen Sie ein Dokument und fügen Sie zwei Klartext-Tags hinzu, die während eines Seriendrucks als MERGEFIELDs fungieren können.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Unsere Tags werden nur dann als Ziele für Serienbriefdaten registriert, wenn wir dies auf „true“ setzen.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Erstellen Sie eine einfache Datentabelle mit einer Spalte.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Siehe auch

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)


