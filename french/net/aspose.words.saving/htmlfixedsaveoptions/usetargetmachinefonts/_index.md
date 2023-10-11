---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlFixedSaveOptions propriété. Lindicateur indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si cet indicateur est défini survrai FontFormat etExportEmbeddedFonts les propriétés nont pas deffet égalementResourceSavingCallback nest pas déclenché pour les polices. La valeur par défaut estFAUX .
type: docs
weight: 190
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

L'indicateur indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si cet indicateur est défini sur`vrai` ,[`FontFormat`](../fontformat/) et[`ExportEmbeddedFonts`](../exportembeddedfonts/) les propriétés n'ont pas d'effet, également[`ResourceSavingCallback`](../resourcesavingcallback/) n'est pas déclenché pour les polices. La valeur par défaut est`FAUX` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

### Exemples

Montre comment utiliser les polices uniquement de la machine cible lors de l'enregistrement d'un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Assemblée [Aspose.Words](../../../)


