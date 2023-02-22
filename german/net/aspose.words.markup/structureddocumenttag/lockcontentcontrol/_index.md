---
title: StructuredDocumentTag.LockContentControl
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag eigendom. Wenn diese Eigenschaft auf true gesetzt ist verhindert sie dass ein Benutzer dies löscht SDT .
type: docs
weight: 190
url: /de/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

Wenn diese Eigenschaft auf „true“ gesetzt ist, verhindert sie, dass ein Benutzer dies löscht **SDT** .

```csharp
public bool LockContentControl { get; set; }
```

### Beispiele

Zeigt, wie Sie Bearbeitungseinschränkungen auf strukturierte Dokument-Tags anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein strukturiertes Klartext-Dokument-Tag ein, das als Textfeld fungiert, das den Benutzer auffordert, es auszufüllen.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft "LockContents" auf "true", um zu verhindern, dass der Benutzer den Inhalt dieses Textfelds bearbeitet.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft "LockContentControl" auf "true", um dem Benutzer dies zu verbieten
// manuelles Löschen dieses strukturierten Dokumenten-Tags in Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


