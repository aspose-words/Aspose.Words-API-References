---
title: FieldRD.IsPathRelative
second_title: Aspose.Words für .NET-API-Referenz
description: FieldRD eigendom. Ruft ab oder legt fest ob der Pfad relativ zum aktuellen Dokument ist.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Ruft ab oder legt fest, ob der Pfad relativ zum aktuellen Dokument ist.

```csharp
public bool IsPathRelative { get; set; }
```

### Beispiele

Zeigt die Verwendung des RD-Felds zum Erstellen eines Inhaltsverzeichniseintrags aus Überschriften in anderen Dokumenten an.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen Document Builder verwenden, um ein Inhaltsverzeichnis einzufügen,
// und fügen Sie dann einen Eintrag für das Inhaltsverzeichnis auf der folgenden Seite hinzu.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Ein RD-Feld einfügen, das in seiner FileName-Eigenschaft auf ein anderes lokales Dateisystemdokument verweist.
// Das Inhaltsverzeichnis akzeptiert jetzt auch alle Überschriften aus dem referenzierten Dokument als Einträge für seine Tabelle.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Erstellen Sie das Dokument, auf das das RD-Feld verweist, und fügen Sie eine Überschrift ein.
// Diese Überschrift wird als Eintrag im TOC-Feld in unserem ersten Dokument angezeigt.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Siehe auch

* class [FieldRD](../)
* namensraum [Aspose.Words.Fields](../../fieldrd/)
* Montage [Aspose.Words](../../../)


