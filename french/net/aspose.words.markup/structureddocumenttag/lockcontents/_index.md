---
title: StructuredDocumentTag.LockContents
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTag propriété. Lorsquelle est définie sur true cette propriété interdit à un utilisateur de modifier le contenu de ce TDS .
type: docs
weight: 200
url: /fr/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

Lorsqu'elle est définie sur true, cette propriété interdit à un utilisateur de modifier le contenu de ce **TDS** .

```csharp
public bool LockContents { get; set; }
```

### Exemples

Montre comment appliquer des restrictions d'édition aux balises de document structuré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une balise de document structuré en texte brut, qui agit comme une zone de texte invitant l'utilisateur à la remplir.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez la propriété "LockContents" sur "true" pour interdire à l'utilisateur de modifier le contenu de cette zone de texte.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez la propriété "LockContentControl" à "true" pour interdire à l'utilisateur de
// suppression manuelle de cette balise de document structuré dans Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttag/)
* Assemblée [Aspose.Words](../../../)


