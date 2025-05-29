---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsPathRelative-Eigenschaft von FieldRD zur einfachen Verwaltung von Dokumentpfaden. Vereinfachen Sie Ihre Programmierung mit flexiblen Pfadeinstellungen für mehr Effizienz!
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Ruft ab oder legt fest, ob der Pfad relativ zum aktuellen Dokument ist.

```csharp
public bool IsPathRelative { get; set; }
```

## Beispiele

Zeigt, wie Sie das RD-Feld verwenden, um aus Überschriften in anderen Dokumenten ein Inhaltsverzeichnis zu erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Dokumentgenerator, um ein Inhaltsverzeichnis einzufügen.
// und fügen Sie dann einen Eintrag für das Inhaltsverzeichnis auf der folgenden Seite hinzu.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Fügen Sie ein RD-Feld ein, das in seiner FileName-Eigenschaft auf ein anderes lokales Dateisystemdokument verweist.
// Das Inhaltsverzeichnis akzeptiert jetzt auch alle Überschriften aus dem referenzierten Dokument als Einträge für seine Tabelle.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

    // Erstellen Sie das Dokument, auf das das RD-Feld verweist, und fügen Sie eine Überschrift ein.
// Diese Überschrift wird als Eintrag im Inhaltsverzeichnisfeld unseres ersten Dokuments angezeigt.
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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
