---
title: MailMerge.UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IFFelds zusammengeführt werden.
type: docs
weight: 140
url: /de/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH` .

### Beispiele

Zeigt, wie Felder oder Regionen unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Füge ein MERGEFIELD ein, das in einem IF-Feld verschachtelt ist.
// Da die IF-Feldanweisung falsch ist, wird das Ergebnis von MERGEFIELD nicht angezeigt.
// Das MERGEFIELD erhält auch bei einem Serienbrief keine Daten.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Wenn wir das Flag „UnconditionalMergeFieldsAndRegions“ auf „true“ setzen,
// Unser Serienbrief fügt Daten in nicht angezeigte Felder wie unser MERGEFIELD und alle anderen ein.
// Wenn wir das Flag „UnconditionalMergeFieldsAndRegions“ auf „false“ setzen,
// Unser Seriendruck fügt keine Daten in MERGEFIELDs ein, die durch IF-Felder mit falschen Anweisungen verdeckt werden.
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
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)


