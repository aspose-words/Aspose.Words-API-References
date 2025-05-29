---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words pour .NET
description: Découvrez la propriété LayoutOptions TextShaperFactory pour une typographie avancée. Améliorez votre rendu grâce à des implémentations ITextShaperFactory personnalisables.
type: docs
weight: 100
url: /fr/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Obtient ou définit[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) implémentation utilisée pour les fonctionnalités de rendu de typographie avancée.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Exemples

Montre comment prendre en charge les fonctionnalités OpenType à l'aide du moteur de mise en forme de texte HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words peut utiliser des objets de mise en forme de texte fournis en externe,
// qui représentent les polices et calculent les informations de mise en forme du texte.
// Une fabrique de mise en forme de texte est nécessaire pour les documents qui utilisent plusieurs polices.
// Lorsque le format de texte est défini en usine, la mise en page utilise les fonctionnalités OpenType.
// Une propriété Instance renvoie un objet BasicTextShaperCache statique enveloppant HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Actuellement, la mise en forme du texte est effectuée lors de l'exportation aux formats PDF ou XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Voir également

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
