---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words pour .NET
description: StructuredDocumentTag IsTemporary propriété. Spécifie si ceciTSD doit être supprimé du document WordProcessingML lorsque son contenu est modifié en C#.
type: docs
weight: 160
url: /fr/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Spécifie si ceci**TSD** doit être supprimé du document WordProcessingML lorsque son contenu est modifié.

```csharp
public bool IsTemporary { get; set; }
```

## Exemples

Montre comment créer des contrôles à usage unique.

```csharp
Document doc = new Document();

// Insère une balise de document structuré en texte brut,
// qui agira comme un formulaire de texte brut dans lequel l'utilisateur pourra saisir du texte.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Définissez la propriété "IsTemporary" sur "true" pour faire disparaître la balise du document structuré et
// assimile son contenu dans le document après que l'utilisateur l'a modifié une fois dans Microsoft Word.
// Définit la propriété "IsTemporary" sur "false" pour permettre à l'utilisateur de modifier le contenu
// de la balise du document structuré un certain nombre de fois.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Insère une autre balise de document structuré sous la forme d'une case à cocher et définit son état par défaut sur "coché".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Définissez la propriété "IsTemporary" sur "true" pour que la case à cocher devienne un symbole
// une fois que l'utilisateur clique dessus dans Microsoft Word.
// Définissez la propriété "IsTemporary" sur "false" pour permettre à l'utilisateur de cliquer sur la case à cocher un certain nombre de fois.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
