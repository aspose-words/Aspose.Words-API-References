---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété LayoutOptions ShowParagraphMarks améliore la mise en forme du texte en activant/désactivant les marques de paragraphe. Améliorez la clarté de vos documents dès aujourd'hui !
type: docs
weight: 90
url: /fr/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Obtient ou définit une indication indiquant si les marques de paragraphe sont rendues. La valeur par défaut est`FAUX` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Exemples

Montre comment afficher les marques de paragraphe dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Ajoutez quelques paragraphes, puis activez les marques de paragraphe pour afficher les fins de paragraphes
// avec un symbole pilcrow (¶) lorsque nous rendons le document.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Voir également

* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
