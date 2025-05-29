---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParagraphFormat OutlineLevel pour définir facilement la hiérarchie des paragraphes dans vos documents, améliorant ainsi l'organisation et la lisibilité.
type: docs
weight: 260
url: /fr/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Spécifie le niveau de plan du paragraphe dans le document.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Exemples

Montre comment configurer les niveaux de plan de paragraphe pour créer du texte réductible.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe a un OutlineLevel, qui peut être n'importe quel nombre de 1 à 9, ou la valeur par défaut « BodyText ».
// La définition de la propriété sur l'une des valeurs numérotées affichera une flèche vers la gauche
// du début du paragraphe.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Le niveau 1 est le niveau le plus élevé. Si un paragraphe de niveau inférieur se trouve sous un paragraphe de niveau supérieur,
// réduire le paragraphe de niveau supérieur réduira le paragraphe de niveau inférieur.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Deux paragraphes du même niveau ne s'effondreront pas l'un l'autre,
// et les flèches ne réduisent pas les paragraphes vers lesquels elles pointent.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// La valeur par défaut de « BodyText » est la plus basse à laquelle un paragraphe de n'importe quel niveau peut se réduire.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Voir également

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
