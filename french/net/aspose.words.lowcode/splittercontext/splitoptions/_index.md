---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words pour .NET
description: Découvrez comment optimiser la gestion de vos documents grâce à la propriété SplitOptions de SplitterContext pour un fractionnement de contenu efficace et flexible. Améliorez votre flux de travail dès aujourd'hui.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Options de fractionnement du document.

```csharp
public SplitOptions SplitOptions { get; }
```

## Exemples

Montre comment diviser un document par pages à l'aide du contexte.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Montre comment diviser le document du flux par pages à l'aide du contexte.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### Voir également

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
