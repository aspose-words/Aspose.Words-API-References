---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „UnconditionalMergeFieldsAndRegions“ von MailMerge die Dokumentautomatisierung verbessert, indem Felder und Regionen ohne bedingte Beschränkungen zusammengeführt werden.
type: docs
weight: 140
url: /de/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt, wie Felder oder Regionen unabhängig vom Zustand des übergeordneten IF-Felds zusammengeführt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEFIELD ein, das in ein IF-Feld verschachtelt ist.
// Da die IF-Feldanweisung falsch ist, wird das Ergebnis von MERGEFIELD nicht angezeigt.
// Auch bei einem Serienbrief werden dem MERGEFIELD keine Daten zugeführt.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Wenn wir das Flag "UnconditionalMergeFieldsAndRegions" auf "true" setzen,
// Unser Serienbrief fügt Daten in nicht angezeigte Felder ein, beispielsweise in unser MERGEFIELD und alle anderen.
// Wenn wir das Flag "UnconditionalMergeFieldsAndRegions" auf "false" setzen,
// Unser Serienbrief fügt keine Daten in MERGEFIELDs ein, die durch IF-Felder mit falschen Anweisungen verborgen sind.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
