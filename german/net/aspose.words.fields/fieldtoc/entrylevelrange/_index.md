---
title: FieldToc.EntryLevelRange
linktitle: EntryLevelRange
articleTitle: EntryLevelRange
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldToc EntryLevelRange“, um die Ebenen Ihres Inhaltsverzeichnisses einfach anzupassen und so die Navigation und das Benutzererlebnis zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldtoc/entrylevelrange/
---
## FieldToc.EntryLevelRange property

Ruft einen Ebenenbereich der einzuschließenden Inhaltsverzeichniseinträge ab oder legt diesen fest.

```csharp
public string EntryLevelRange { get; set; }
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

* class [FieldToc](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
