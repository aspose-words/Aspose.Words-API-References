---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveFormat d'OoxmlSaveOptions pour choisir facilement des formats de documents tels que Docx, Docm, Dotx, Dotm ou FlatOpc pour une sauvegarde transparente.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreDocx ,Docm , Dotx ,Dotm ouFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exemples

Montre comment définir une spécification de conformité OOXML à laquelle un document enregistré doit adhérer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour être conformes à Microsoft Word 2003,
// l'insertion d'une image définira sa forme à l'aide de VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML « ISO/IEC 29500:2008 » ne prend pas en charge les formes VML.
// Si nous définissons la propriété « Compliance » de l'objet SaveOptions sur « OoxmlCompliance.Iso29500_2008_Strict »,
 // tout document que nous sauvegardons en passant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour adhérer à la norme OOXML « ISO/IEC 29500:2008 ».
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
