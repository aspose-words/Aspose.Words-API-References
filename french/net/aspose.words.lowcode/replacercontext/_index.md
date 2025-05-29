---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words LowCode ReplacerContext pour des opérations de recherche et de remplacement transparentes, améliorant l'automatisation et l'efficacité de vos documents.
type: docs
weight: 4350
url: /fr/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

Contexte de l'opération Rechercher/remplacer.

```csharp
public class ReplacerContext : ProcessorContext
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | Options de recherche/remplacement. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Paramètres de police utilisés par le processeur. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Options de mise en page du document utilisées par le processeur. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Rappel d'avertissement utilisé par le processeur. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | Définit le modèle et le remplacement utilisés par l'opération de recherche/remplacement. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | Définit le modèle et le remplacement utilisés par l'opération de recherche/remplacement. |

## Exemples

Montre comment remplacer une chaîne par une expression régulière dans le document à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document :
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

Montre comment remplacer une chaîne dans le document à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document :
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

Montre comment remplacer une chaîne dans le document à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne dans le document à l'aide de documents du flux :
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

Montre comment remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons de remplacer une chaîne par une expression régulière dans le document à l'aide de documents du flux :
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* class [ProcessorContext](../processorcontext/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
