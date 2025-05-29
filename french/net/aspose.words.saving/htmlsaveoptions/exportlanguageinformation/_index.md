---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: Aspose.Words pour .NET
description: Contrôlez l'exportation des langues au format HTML, MHTML ou EPUB avec HtmlSaveOptions. Améliorez l'accessibilité de vos documents et touchez un public plus large sans effort.
type: docs
weight: 180
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Spécifie si les informations de langue sont exportées au format HTML, MHTML ou EPUB. La valeur par défaut est`FAUX` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

## Remarques

Lorsque cette propriété est définie sur`vrai` Sorties Aspose.Words**langue**Attribut HTML sur les éléments document spécifiant la langue. Cela peut être nécessaire pour préserver la sémantique liée à la langue.

## Exemples

Montre comment conserver les informations de langue lors de l'enregistrement au format .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez le générateur pour écrire du texte tout en le formatant dans différents paramètres régionaux.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// Lors de l'enregistrement du document au format HTML, nous pouvons passer un objet SaveOptions
// pour conserver ou supprimer les paramètres régionaux de chaque texte formaté.
// Si nous définissons l'indicateur « ExportLanguageInformation » sur « true »,
// le document HTML de sortie contiendra les paramètres régionaux dans les attributs « lang » des balises <span>.
// Si nous définissons l'indicateur « ExportLanguageInformation » sur « false »,
// le texte dans le document HTML de sortie ne contiendra aucune information de paramètres régionaux.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
