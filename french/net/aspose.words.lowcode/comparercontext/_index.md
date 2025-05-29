---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words LowCode ComparerContext pour une comparaison efficace des documents, améliorant votre flux de travail avec une intégration transparente et des fonctionnalités puissantes.
type: docs
weight: 4220
url: /fr/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Comparateur de documents context

```csharp
public class ComparerContext : ProcessorContext
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ComparerContext](comparercontext/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Indique s'il faut accepter les révisions dans les documents avant de les comparer. Si les documents comparés contiennent des révisions et que cet indicateur est défini sur faux, le processeur rejettera les révisions. La valeur par défaut est`vrai` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | L'auteur à attribuer aux révisions créées lors de la comparaison des documents. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Options utilisées lors de la comparaison de documents. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | La date et l'heure attribuées aux révisions créées lors de la comparaison des documents. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Paramètres de police utilisés par le processeur. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Options de mise en page du document utilisées par le processeur. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Rappel d'avertissement utilisé par le processeur. |

## Exemples

Montre comment comparer simplement des documents en utilisant le contexte.

```csharp
// Il existe plusieurs façons de comparer des documents :
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Montre comment comparer des documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons de comparer les documents du flux :
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Voir également

* class [ProcessorContext](../processorcontext/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
