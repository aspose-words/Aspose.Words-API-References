---
title: StructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words für .NET
description: StructuredDocumentTag LockContents eigendom. Wenn eingestellt aufWAHR  verhindert diese Eigenschaft dass ein Benutzer den Inhalt dieser Datei bearbeitetSDT  in C#.
type: docs
weight: 200
url: /de/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

Wenn eingestellt auf`WAHR` , verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieser Datei bearbeitet**SDT** .

```csharp
public bool LockContents { get; set; }
```

## Beispiele

Zeigt, wie Bearbeitungsbeschränkungen auf strukturierte Dokument-Tags angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein strukturiertes Nur-Text-Dokument-Tag ein, das als Textfeld fungiert, das den Benutzer zum Ausfüllen auffordert.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft „LockContents“ auf „true“, um zu verhindern, dass der Benutzer den Inhalt dieses Textfelds bearbeitet.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft „LockContentControl“ auf „true“, um dem Benutzer dies zu verbieten
// Dieses strukturierte Dokument-Tag manuell in Microsoft Word löschen.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
