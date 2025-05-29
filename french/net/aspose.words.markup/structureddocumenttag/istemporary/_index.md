---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété StructuredDocumentTag IsTemporary détermine si votre SDT est supprimé de WordProcessingML en cas de modification de contenu. Optimisez vos documents dès aujourd'hui !
type: docs
weight: 160
url: /fr/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Spécifie si cela**SDT** sera supprimé du document WordProcessingML lorsque son contenu sera modifié.

```csharp
public bool IsTemporary { get; set; }
```

## Exemples

Montre comment réaliser des contrôles à usage unique.

```csharp
Document doc = new Document();

// Insérer une balise de document structurée en texte brut,
// qui agira comme un formulaire de texte brut dans lequel l'utilisateur pourra saisir du texte.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez la propriété « IsTemporary » sur « true » pour faire disparaître la balise de document structuré et
// assimiler son contenu dans le document après que l'utilisateur l'a modifié une fois dans Microsoft Word.
// Définissez la propriété « IsTemporary » sur « false » pour permettre à l'utilisateur de modifier le contenu
// de la balise de document structuré un nombre quelconque de fois.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Insérez une autre balise de document structuré sous la forme d'une case à cocher et définissez son état par défaut sur « coché ».
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Définissez la propriété « IsTemporary » sur « true » pour que la case à cocher devienne un symbole
// une fois que l'utilisateur clique dessus dans Microsoft Word.
// Définissez la propriété « IsTemporary » sur « false » pour permettre à l'utilisateur de cliquer sur la case à cocher autant de fois que nécessaire.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
