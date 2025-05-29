---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlSaveOptions ExportDropDownFormFieldAsText optimise vos exportations HTML/MHTML en contrôlant les formats des champs déroulants. Optimisez vos documents !
type: docs
weight: 130
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Contrôle la manière dont les champs de formulaire déroulant sont enregistrés au format HTML ou MHTML. La valeur par défaut est`FAUX` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Remarques

Lorsqu'il est réglé sur`vrai` , exporte les champs de formulaire déroulants sous forme de texte normal. Lorsque`FAUX`, exporte les champs de formulaire déroulants en tant qu'élément SELECT en HTML.

Lors de l'exportation vers EPUB, les champs de formulaire déroulants de texte sont toujours enregistrés sous forme de texte en raison des exigences de ce format.

## Exemples

Montre comment faire en sorte que les champs de formulaire de zone de liste déroulante se fondent dans le texte du paragraphe lors de l'enregistrement au format HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de documents pour insérer une zone de liste déroulante avec la valeur « Deux » sélectionnée.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// L'indicateur "ExportDropDownFormFieldAsText" de cet objet SaveOptions nous permet de
// contrôler la manière dont l'enregistrement du document au format HTML traite les zones de liste déroulante.
// Le définir sur « true » convertira chaque zone de liste déroulante en texte simple
// qui affiche la valeur actuellement sélectionnée de la zone de liste déroulante, la gelant ainsi efficacement.
// Le définir sur « false » préservera la fonctionnalité de la zone de liste déroulante utilisant les balises <select> et <option>.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
