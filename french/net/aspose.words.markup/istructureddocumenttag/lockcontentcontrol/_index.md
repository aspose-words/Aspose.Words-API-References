---
title: IStructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IStructuredDocumentTag LockContentControl. Définie sur « true », elle empêche les utilisateurs de supprimer les SDT, améliorant ainsi l'intégrité et le contrôle des documents.
type: docs
weight: 70
url: /fr/net/aspose.words.markup/istructureddocumenttag/lockcontentcontrol/
---
## IStructuredDocumentTag.LockContentControl property

Lorsqu'elle est définie sur true, cette propriété interdira à un utilisateur de supprimer ceci**SDT** .

```csharp
public bool LockContentControl { get; set; }
```

## Exemples

Montre comment appliquer des restrictions d'édition aux balises de documents structurés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une balise de document structurée en texte brut, qui agit comme une zone de texte invitant l'utilisateur à la remplir.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez la propriété « LockContents » sur « true » pour interdire à l'utilisateur de modifier le contenu de cette zone de texte.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez la propriété « LockContentControl » sur « true » pour interdire à l'utilisateur de
// suppression manuelle de cette balise de document structuré dans Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Voir également

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
