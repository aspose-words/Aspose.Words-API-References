---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words für .NET
description: MailMerge UseNonMergeFields eigendom. WannWAHR  gibt an dass der Seriendruck zusätzlich zu MERGEFIELDFeldern auch in einigen anderen Feldtypen und auch in fieldNameTags durchgeführt wird in C#.
type: docs
weight: 150
url: /de/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Wann`WAHR` , gibt an, dass der Seriendruck zusätzlich zu MERGEFIELD-Feldern auch in einigen anderen Feldtypen und auch in „{{fieldName}}“-Tags durchgeführt wird.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Bemerkungen

Normalerweise wird der Seriendruck nur in MERGEFIELD-Feldern durchgeführt, aber bei mehreren Kunden wurde das Reporting mit anderen Feldern erstellt und viele Dokumente wurden auf diese Weise erstellt. Um die Migration zu vereinfachen (und weil dieser -Ansatz von mehreren Kunden unabhängig voneinander verwendet wurde), wurde die Möglichkeit eingeführt, Serienbriefe in andere Felder zu übertragen.

Wann`UseNonMergeFields` ist eingestellt auf`WAHR`, Aspose.Words führt einen Serienbrief in den folgenden Feldern durch:

MERGEFIELD Feldname

MACROBUTTON NOMACRO FieldName

WENN 0 = 0 „{FieldName}“ „“

Auch wann`UseNonMergeFields` ist eingestellt auf`WAHR`, Aspose.Words führt einen Seriendruck in Text-Tags „{{fieldName}}“ durch. Dabei handelt es sich nicht um Felder, sondern nur um Text-Tags.

## Beispiele

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

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
