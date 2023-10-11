---
title: ParagraphFormat.LinesToDrop
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Obtient ou définit le nombre de lignes du texte du paragraphe utilisé pour calculer la hauteur des lettrines.
type: docs
weight: 210
url: /fr/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Obtient ou définit le nombre de lignes du texte du paragraphe utilisé pour calculer la hauteur des lettrines.

```csharp
public int LinesToDrop { get; set; }
```

### Exemples

Montre comment définir la taille d’une lettrine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifier la propriété "LinesToDrop" pour désigner un paragraphe en lettrine,
// ce qui le transformera en une grande lettre majuscule qui décorera le paragraphe suivant.
// Donnez à cette propriété la valeur 4 pour donner à la lettrine la hauteur de quatre lignes de texte.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Réinitialise la propriété "LinesToDrop" à 0 pour transformer le paragraphe suivant en paragraphe ordinaire.
// Le texte de ce paragraphe entourera la lettrine.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


