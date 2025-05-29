---
title: FieldTC.TypeIdentifier
linktitle: TypeIdentifier
articleTitle: TypeIdentifier
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldTC TypeIdentifier-Eigenschaft. Verwalten Sie Feldtypkennungen ganz einfach mit dieser vielseitigen Funktion und verbessern Sie so Ihre Datenorganisation und -effizienz.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

Ruft eine Typkennung für dieses Feld ab oder legt sie fest (normalerweise ein Buchstabe).

```csharp
public string TypeIdentifier { get; set; }
```

## Beispiele

Zeigt, wie ein Inhaltsverzeichnisfeld eingefügt wird und wie gefiltert wird, welche TC-Felder als Einträge enden.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie ein TOC-Feld ein, das alle TC-Felder in einem Inhaltsverzeichnis zusammenfasst.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Konfigurieren Sie das Feld so, dass nur TC-Einträge des Typs „A“ und einer Eintragsebene zwischen 1 und 3 aufgenommen werden.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Diese beiden Einträge werden in der Tabelle angezeigt.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Dieser Eintrag wird aus der Tabelle weggelassen, da er einen anderen Typ als „A“ hat.
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Dieser Eintrag wird aus der Tabelle weggelassen, da er eine Eintragsebene außerhalb des Bereichs 1-3 hat.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Verwenden Sie einen Dokumentgenerator, um ein TC-Feld einzufügen.
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
