---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.LowCode.SplitterContext pour un fractionnement efficace des documents, améliorant votre flux de travail avec une intégration transparente et des fonctionnalités puissantes.
type: docs
weight: 4430
url: /fr/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Contexte du séparateur de documents.

```csharp
public class SplitterContext : ProcessorContext
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [SplitterContext](splittercontext/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Paramètres de police utilisés par le processeur. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Options de mise en page du document utilisées par le processeur. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Options de fractionnement du document. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Rappel d'avertissement utilisé par le processeur. |

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

* class [ProcessorContext](../processorcontext/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
