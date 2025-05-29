---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété UseTargetMachineFonts de HtmlFixedSaveOptions améliore l'affichage des documents en utilisant les polices de la machine cible. Optimisez votre gestion des polices dès aujourd'hui !
type: docs
weight: 210
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

L'indicateur indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si cet indicateur est défini sur`vrai` ,[`FontFormat`](../fontformat/) et[`ExportEmbeddedFonts`](../exportembeddedfonts/) les propriétés n'ont pas d'effet, aussi[`ResourceSavingCallback`](../resourcesavingcallback/) n'est pas déclenché pour les polices. La valeur par défaut est`FAUX` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Exemples

Montre comment utiliser uniquement les polices de la machine cible lors de l'enregistrement d'un document au format HTML.

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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
