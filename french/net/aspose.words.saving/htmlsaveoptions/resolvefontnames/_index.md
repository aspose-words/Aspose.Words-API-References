---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ResolveFontNames propriété. Spécifie si les noms de familles de polices utilisés dans le document sont résolus et remplacés conformément à FontSettings lors de lécriture dans des formats HTML en C#.
type: docs
weight: 410
url: /fr/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Spécifie si les noms de familles de polices utilisés dans le document sont résolus et remplacés conformément à [`FontSettings`](../../../aspose.words/document/fontsettings/) lors de l'écriture dans des formats HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

## Remarques

Par défaut, cette option est définie sur`FAUX` et les noms de familles de polices sont écrits au format HTML sous la forme spécifiée dans les documents sources. C'est,[`FontSettings`](../../../aspose.words/document/fontsettings/) sont ignorés et aucune résolution ou substitution des noms de famille de polices n'est effectuée.

Si cette option est définie sur`vrai` , Aspose.Words utilise[`FontSettings`](../../../aspose.words/document/fontsettings/) pour résoudre chaque nom de famille de polices spécifié dans un document source en nom d'une famille de polices disponible, en effectuant la substitution de police selon les besoins.

## Exemples

Montre comment résoudre tous les noms de polices avant de les écrire au format HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Ce document contient du texte qui nomme une police que nous n'avons pas.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Si nous n'avons aucun moyen d'obtenir cette police et que nous voulons pouvoir afficher tout le texte
// dans ce document dans une sortie HTML, nous pouvons le remplacer par une autre police.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // Par défaut, cette option est définie sur 'False' et Aspose.Words écrit les noms de police comme spécifié dans le document source
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
