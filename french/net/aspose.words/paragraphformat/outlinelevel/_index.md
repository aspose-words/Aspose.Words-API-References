---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words pour .NET
description: ParagraphFormat OutlineLevel propriété. Spécifie le niveau de plan du paragraphe dans le document en C#.
type: docs
weight: 250
url: /fr/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Spécifie le niveau de plan du paragraphe dans le document.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Exemples

Montre comment configurer les niveaux de plan de paragraphe pour créer du texte pliable.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe a un OutlineLevel, qui peut être n'importe quel nombre compris entre 1 et 9, ou la valeur par défaut "BodyText".
// Définir la propriété sur l'une des valeurs numérotées affichera une flèche vers la gauche
// du début du paragraphe.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Le niveau 1 est le niveau le plus élevé. S'il y a un paragraphe de niveau inférieur en dessous d'un paragraphe de niveau supérieur,
// la réduction du paragraphe de niveau supérieur réduira le paragraphe de niveau inférieur.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Deux paragraphes de même niveau ne se réduiront pas,
// et les flèches ne réduisent pas les paragraphes vers lesquels elles pointent.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// La valeur par défaut de "BodyText" est la plus basse qu'un paragraphe de n'importe quel niveau peut réduire.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Voir également

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
