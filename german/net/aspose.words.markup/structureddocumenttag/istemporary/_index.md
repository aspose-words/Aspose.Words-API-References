---
title: StructuredDocumentTag.IsTemporary
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag eigendom. Gibt an ob dies der Fall ist SDT wird aus dem WordProcessingMLDokument entfernt wenn dessen Inhalt geändert wird.
type: docs
weight: 160
url: /de/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Gibt an, ob dies der Fall ist **SDT** wird aus dem WordProcessingML-Dokument entfernt, wenn dessen Inhalt geändert wird.

```csharp
public bool IsTemporary { get; set; }
```

### Beispiele

Zeigt, wie Einwegsteuerelemente erstellt werden.

```csharp
Document doc = new Document();

// Ein strukturiertes Nur-Text-Dokument-Tag einfügen,
// das als reines Textformular fungiert, in das der Benutzer Text eingeben kann.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft „IsTemporary“ auf „true“, damit das strukturierte Dokument-Tag verschwindet und
// seinen Inhalt in das Dokument integrieren, nachdem der Benutzer ihn einmal in Microsoft Word bearbeitet hat.
// Setzen Sie die Eigenschaft „IsTemporary“ auf „false“, damit der Benutzer den Inhalt bearbeiten kann
// des strukturierten Dokument-Tags beliebig oft.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Fügen Sie ein weiteres strukturiertes Dokument-Tag in Form eines Kontrollkästchens ein und setzen Sie dessen Standardstatus auf „aktiviert“.
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Setzen Sie die Eigenschaft „IsTemporary“ auf „true“, damit das Kontrollkästchen zu einem Symbol wird
// sobald der Benutzer in Microsoft Word darauf klickt.
// Setzen Sie die Eigenschaft „IsTemporary“ auf „false“, damit der Benutzer beliebig oft auf das Kontrollkästchen klicken kann.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


