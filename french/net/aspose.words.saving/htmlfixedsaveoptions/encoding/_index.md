---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words pour .NET
description: HtmlFixedSaveOptions Encoding propriété. Spécifie lencodage à utiliser lors de lexportation au format HTML. La valeur par défaut estnouveau codage UTF8 vrai UTF8 avec nomenclature en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Spécifie l'encodage à utiliser lors de l'exportation au format HTML. La valeur par défaut est`nouveau codage UTF8 (vrai)` (UTF-8 avec nomenclature).

```csharp
public Encoding Encoding { get; set; }
```

## Exemples

Montre comment définir le codage à utiliser lors de l'exportation d'un document au format HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// L'encodage par défaut est UTF-8. Si nous voulons représenter notre document en utilisant un encodage différent,
// nous pouvons utiliser un objet SaveOptions pour définir un encodage spécifique.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
