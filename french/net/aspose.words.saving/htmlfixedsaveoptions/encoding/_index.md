---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words pour .NET
description: Découvrez la propriété d'encodage HtmlFixedSaveOptions pour des exportations HTML fluides. Configurez facilement l'encodage UTF-8 avec BOM pour une intégrité optimale des données.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

Spécifie l'encodage à utiliser lors de l'exportation au format HTML. La valeur par défaut est`nouveau UTF8Encoding(true)` (UTF-8 avec BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Exemples

Montre comment définir l'encodage à utiliser lors de l'exportation d'un document au format HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// L'encodage par défaut est UTF-8. Si nous souhaitons représenter notre document avec un encodage différent,
// nous pouvons utiliser un objet SaveOptions pour définir un encodage spécifique.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
