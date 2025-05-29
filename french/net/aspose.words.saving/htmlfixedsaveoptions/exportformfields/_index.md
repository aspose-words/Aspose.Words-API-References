---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlFixedSaveOptions ExportFormFields améliore vos exportations de documents en gardant les champs de formulaire interactifs, améliorant ainsi l'expérience utilisateur.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Obtient ou définit une indication indiquant si les champs de formulaire sont exportés en tant qu'éléments interactifs (en tant que balise « input ») plutôt que convertis en texte ou en graphiques.

```csharp
public bool ExportFormFields { get; set; }
```

## Exemples

Montre comment exporter des champs de formulaire vers HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Lorsque nous exportons un document avec des champs de formulaire vers .html,
// il existe deux manières par lesquelles Aspose.Words peut exporter des champs de formulaire.
// Définir l'indicateur « ExportFormFields » sur « true » les exportera en tant qu'objets interactifs.
// La définition de cet indicateur sur « false » affichera les champs du formulaire sous forme de texte brut.
// Cela les gèlera à leur valeur actuelle et empêchera le lecteur de notre document HTML
// de pouvoir interagir avec eux.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
