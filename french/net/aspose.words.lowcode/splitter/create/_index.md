---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words pour .NET
description: Découvrez comment créer efficacement une nouvelle instance du processeur séparateur avec notre guide facile à suivre pour une intégration transparente et des performances améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Crée une nouvelle instance du processeur séparateur.

```csharp
public static Splitter Create(SplitterContext context)
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

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
