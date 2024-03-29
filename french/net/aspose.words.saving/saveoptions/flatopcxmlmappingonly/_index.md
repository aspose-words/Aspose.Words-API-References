---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés parXmlMapping . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Remarques

Cette option est associée à[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . En règle générale, vous devez définir les deux sur false pour autoriser le mappage de formats de document arbitraires.

### Exemples

Montre comment lier des balises de document structuré à n'importe quel format.

```csharp
// Si vrai - SDT contiendra du texte HTML brut.
// Si false - le HTML mappé sera analysé et le document résultant sera inséré dans le contenu SDT.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


