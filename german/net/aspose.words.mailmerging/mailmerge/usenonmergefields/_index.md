---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words für .NET
description: Nutzen Sie die Möglichkeiten von MailMerge! Nutzen Sie die Eigenschaft UseNonMergeFields, um Ihre Dokumente durch die nahtlose Zusammenführung verschiedener Feldtypen zu optimieren.
type: docs
weight: 150
url: /de/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Wann`WAHR` , gibt an, dass Serienbriefe zusätzlich zu MERGEFIELD-Feldern auch in einigen anderen Feldtypen und auch in "{{fieldName}}"-Tags ausgeführt werden.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Bemerkungen

Normalerweise wird Serienbriefe nur in MERGEFIELD-Feldern ausgeführt, aber einige Kunden hatten ihre Berichte mit anderen Feldern erstellt und viele Dokumente auf diese Weise erstellt. Um die Migration zu vereinfachen (und weil dieser -Ansatz von mehreren Kunden unabhängig voneinander genutzt wurde), wurde die Möglichkeit eingeführt, Serienbriefe in andere Felder zu übertragen.

Wann`UseNonMergeFields` ist eingestellt auf`WAHR`, Aspose.Words führt Serienbriefe in den folgenden Feldern durch:

MERGEFIELD Feldname

MACROBUTTON NOMACRO Feldname

WENN 0 = 0 "{Feldname}" ""

Auch wenn`UseNonMergeFields` ist eingestellt auf`WAHR`Aspose.Words führt Serienbriefe in Text-Tags "{{fieldName}}" durch. Dabei handelt es sich nicht um Felder, sondern lediglich um Text-Tags.

## Beispiele

Zeigt, wie das Erscheinungsbild alternativer Serienbrief-Tags beibehalten wird, die während eines Serienbriefs nicht verwendet werden.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

        // Standardmäßig platziert ein Serienbrief Daten aus jeder Zeile einer Tabelle in MERGEFIELDs, die Spalten in dieser Tabelle benennen.
    // Unser Dokument hat keine solchen Felder, aber es hat Klartext-Tags, die in geschweifte Klammern eingeschlossen sind.
    // Wenn wir das Flag "PreserveUnusedTags" auf "true" setzen, könnten wir diese Tags als MERGEFIELDs behandeln
    // um unserem Serienbrief zu ermöglichen, an diesen Tags Daten aus der Datenquelle einzufügen.
    // Wenn wir das Flag "PreserveUnusedTags" auf "false" setzen,
    // Der Serienbrief konvertiert diese Tags in MERGEFIELDs und lässt sie leer.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Unser Dokument hat ein Tag für eine Spalte mit dem Namen „Column2“, die in der Tabelle nicht vorhanden ist.
    // Wenn wir das Flag „PreserveUnusedTags“ auf „false“ setzen, dann konvertiert der Serienbrief dieses Tag in ein MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Erstellen Sie ein Dokument und fügen Sie zwei Klartext-Tags hinzu, die während eines Serienbriefs als MERGEFIELDs fungieren können.
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
