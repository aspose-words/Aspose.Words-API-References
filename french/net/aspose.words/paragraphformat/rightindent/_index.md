---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: Aspose.Words pour .NET
description: Découvrez comment ajuster facilement le retrait correct de vos paragraphes grâce à la propriété ParagraphFormat RightIndent. Améliorez la mise en forme de vos documents dès aujourd'hui !
type: docs
weight: 280
url: /fr/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Obtient ou définit la valeur (en points) qui représente le retrait correct du paragraphe.

```csharp
public double RightIndent { get; set; }
```

## Exemples

Montre comment configurer la mise en forme des paragraphes pour créer du texte décentré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Centrez tout le texte écrit par le générateur de documents et définissez les retraits.
// La configuration d'indentation ci-dessous créera un corps de texte qui sera placé de manière asymétrique sur la page.
// Le « centre » sur lequel nous alignons le texte sera le milieu du corps du texte, pas le milieu de la page.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
