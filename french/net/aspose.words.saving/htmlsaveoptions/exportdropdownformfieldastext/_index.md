---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ExportDropDownFormFieldAsText propriété. Contrôle la façon dont les champs du formulaire déroulant sont enregistrés au format HTML ou MHTML. La valeur par défaut estFAUX  en C#.
type: docs
weight: 130
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Contrôle la façon dont les champs du formulaire déroulant sont enregistrés au format HTML ou MHTML. La valeur par défaut est`FAUX` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Remarques

Lorsqu'il est réglé sur`vrai` , exporte les champs du formulaire déroulant sous forme de texte normal. Lorsque`FAUX`, exporte les champs du formulaire déroulant en tant qu'élément SELECT en HTML.

Lors de l'exportation vers EPUB, les champs du formulaire déroulant de texte sont toujours enregistrés sous forme de texte en raison des exigences de ce format.

## Exemples

Montre comment faire en sorte que les champs de formulaire de liste déroulante se fondent dans le texte du paragraphe lors de l'enregistrement au format HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de documents pour insérer une zone de liste déroulante avec la valeur "Deux" sélectionnée.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Le flag "ExportDropDownFormFieldAsText" de cet objet SaveOptions nous permet de
// contrôle la façon dont l'enregistrement du document au format HTML traite les listes déroulantes.
// Le définir sur "true" convertira chaque zone de liste déroulante en texte simple
// qui affiche la valeur actuellement sélectionnée de la zone de liste déroulante, la gelant ainsi.
// Le définir sur "false" préservera la fonctionnalité de la zone de liste déroulante en utilisant <select> et <option> Mots clés.
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
