---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font NumberSpacing pour personnaliser l'espacement des chiffres et améliorer la lisibilité et le design. Optimisez votre typographie dès aujourd'hui !
type: docs
weight: 290
url: /fr/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Obtient ou définit le type d'espacement du chiffre affiché.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Exemples

Montre comment définir le type d'espacement du chiffre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cet effet n'est pris en charge que dans les versions plus récentes de MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Voir également

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
