---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions ResolveFontNames améliore la mise en forme des documents en garantissant des substitutions de polices précises dans les sorties HTML.
type: docs
weight: 430
url: /fr/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Spécifie si les noms de familles de polices utilisés dans le document sont résolus et substitués conformément à [`FontSettings`](../../../aspose.words/document/fontsettings/) lorsqu'ils sont écrits dans des formats basés sur HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

## Remarques

Par défaut, cette option est définie sur`FAUX` et les noms de familles de polices sont écrits en HTML sous la forme specified dans les documents sources. Autrement dit,[`FontSettings`](../../../aspose.words/document/fontsettings/) sont ignorés et aucune résolution ou substitution des noms de famille de polices n'est effectuée.

Si cette option est définie sur`vrai` , Aspose.Words utilise[`FontSettings`](../../../aspose.words/document/fontsettings/) pour résoudre chaque nom de famille de polices spécifié dans un document source dans le nom d'une famille de polices disponible, en effectuant une substitution de police si nécessaire.

## Exemples

Montre comment résoudre tous les noms de polices avant de les écrire en HTML.

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
    // Par défaut, cette option est définie sur « False » et Aspose.Words écrit les noms de police tels que spécifiés dans le document source
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
