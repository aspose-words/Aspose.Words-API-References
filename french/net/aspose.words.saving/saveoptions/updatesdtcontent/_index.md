---
title: SaveOptions.UpdateSdtContent
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Obtient ou définit la valeur déterminant si le contenu deStructuredDocumentTag est mis à jour avant lenregistrement.
type: docs
weight: 200
url: /fr/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Remarques

La valeur par défaut est`vrai` .

### Exemples

Montre comment mettre à jour les balises de document structuré lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();

// Insère une balise de document structurée en liste déroulante.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// La liste déroulante affiche actuellement "Choose an item" comme texte par défaut.
// Définissez la propriété "SelectedValue" sur l'un des éléments de la liste pour obtenir la balise
// affiche la valeur de cet élément de liste au lieu du texte par défaut.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Crée un objet "PdfSaveOptions" à passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode enregistre le document au format .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "UpdateSdtContent" à "false" pour ne pas mettre à jour les balises du document structuré
// lors de l'enregistrement du document au format PDF. Ils afficheront leurs valeurs par défaut telles qu'elles étaient au moment de la construction.
// Définissez la propriété "UpdateSdtContent" sur "true" pour vous assurer que les balises affichent les valeurs mises à jour dans le PDF.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


