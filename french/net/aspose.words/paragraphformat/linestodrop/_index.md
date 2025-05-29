---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ParagraphFormat LinesToDrop améliore la hauteur des lettrines dans vos documents. Optimisez la mise en page de votre texte pour des visuels époustouflants !
type: docs
weight: 210
url: /fr/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Obtient ou définit le nombre de lignes du texte du paragraphe utilisé pour calculer la hauteur de la lettrine.

```csharp
public int LinesToDrop { get; set; }
```

## Exemples

Montre comment définir la taille d'une lettrine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifiez la propriété « LinesToDrop » pour désigner un paragraphe comme une lettrine,
// qui le transformera en une grande lettre majuscule qui décorera le paragraphe suivant.
// Donnez à cette propriété une valeur de 4 pour donner à la lettrine la hauteur de quatre lignes de texte.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Réinitialisez la propriété « LinesToDrop » à 0 pour transformer le paragraphe suivant en un paragraphe ordinaire.
// Le texte de ce paragraphe s'enroulera autour de la lettrine.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
