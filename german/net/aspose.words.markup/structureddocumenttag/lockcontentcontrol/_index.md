---
title: StructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „StructuredDocumentTag LockContentControl“ die Dokumentsicherheit erhöht, indem sie Benutzer daran hindert, wichtige Inhalte zu löschen. Erfahren Sie mehr!
type: docs
weight: 190
url: /de/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

Wenn eingestellt auf`WAHR` , verhindert diese Eigenschaft, dass ein Benutzer diese**SDT** .

```csharp
public bool LockContentControl { get; set; }
```

## Beispiele

Zeigt, wie Bearbeitungsbeschränkungen auf strukturierte Dokument-Tags angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einen strukturierten Dokument-Tag im Klartext ein, der als Textfeld fungiert und den Benutzer zum Ausfüllen auffordert.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft „LockContents“ auf „true“, um dem Benutzer das Bearbeiten des Inhalts dieses Textfelds zu verbieten.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft "LockContentControl" auf "true", um dem Benutzer zu verbieten,
// dieses strukturierte Dokument-Tag manuell in Microsoft Word löschen.
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
