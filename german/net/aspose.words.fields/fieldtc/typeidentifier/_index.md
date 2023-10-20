---
title: FieldTC.TypeIdentifier
linktitle: TypeIdentifier
articleTitle: TypeIdentifier
second_title: Aspose.Words für .NET
description: FieldTC TypeIdentifier eigendom. Ruft einen Typbezeichner für dieses Feld ab normalerweise ein Buchstabe oder legt diesen fest in C#.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

Ruft einen Typbezeichner für dieses Feld ab (normalerweise ein Buchstabe) oder legt diesen fest.

```csharp
public string TypeIdentifier { get; set; }
```

## Beispiele

Zeigt, wie man ein TOC-Feld einfügt und filtert, welche TC-Felder als Einträge enden.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ein TOC-Feld einfügen, das alle TC-Felder in einem Inhaltsverzeichnis zusammenstellt.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Konfigurieren Sie das Feld nur für die Aufnahme von TC-Einträgen vom Typ „A“ und einer Eintragsebene zwischen 1 und 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Diese beiden Einträge werden in der Tabelle angezeigt.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Dieser Eintrag wird in der Tabelle weggelassen, da er einen anderen Typ als „A“ hat.
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Dieser Eintrag wird in der Tabelle weggelassen, da sein Eintragsniveau außerhalb des Bereichs 1-3 liegt.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Verwenden Sie einen Document Builder, um ein TC-Feld einzufügen.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Siehe auch

* class [FieldTC](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
