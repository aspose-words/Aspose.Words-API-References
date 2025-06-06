---
title: OoxmlSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words pour .NET
description: Découvrez la conformité OoxmlSaveOptions pour choisir la version OOXML de vos documents de sortie. Optimisez vos fichiers avec le paramètre Ecma376_2006 par défaut.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/compliance/
---
## OoxmlSaveOptions.Compliance property

Spécifie la version OOXML du document de sortie. La valeur par défaut estEcma376_2006 .

```csharp
public OoxmlCompliance Compliance { get; set; }
```

## Exemples

Montre comment insérer des formes DML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'emballage que les formes peuvent avoir.
// 1 - Flottant :
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En ligne :
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si vous devez créer des formes « non primitives », telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// Coins supérieurs un arrondi un coupé, Coin unique arrondi, Coins supérieurs arrondis ou Coins diagonaux arrondis,
// puis enregistrez le document avec une conformité « Stricte » ou « Transitionnelle », ce qui permet d'enregistrer la forme au format DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Montre comment configurer une liste pour redémarrer la numérotation à chaque section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// La propriété « IsRestartAtEachSection » ne sera applicable que lorsque
// le niveau de conformité OOXML du document est conforme à une norme plus récente que « OoxmlComplianceCore.Ecma376 ».
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

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

* enum [OoxmlCompliance](../../ooxmlcompliance/)
* class [OoxmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
