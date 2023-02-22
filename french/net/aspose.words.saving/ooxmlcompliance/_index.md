---
title: Enum OoxmlCompliance
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.OoxmlCompliance énumération. Permet de spécifier quelle spécification OOXML sera utilisée lors de lenregistrement au format DOCX.
type: docs
weight: 5060
url: /fr/net/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enumeration

Permet de spécifier quelle spécification OOXML sera utilisée lors de l'enregistrement au format DOCX.

```csharp
public enum OoxmlCompliance
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Ecma376_2006 | `0` | ECMA-376 1ère édition, 2006. |
| Iso29500_2008_Transitional | `1` | ISO/IEC 29500:2008 Niveau de conformité transitoire. |
| Iso29500_2008_Strict | `2` | ISO/IEC 29500:2008 Niveau de conformité stricte. |

### Exemples

Montre comment insérer des formes DML dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'habillage que les formes peuvent avoir.
// 1 - Flottant :
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En ligne :
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si vous avez besoin de créer des formes "non primitives", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded ou DiagonalCornersRounded,
// puis enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme au format DML.
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

// La propriété "IsRestartAtEachSection" ne sera applicable que lorsque
// le niveau de conformité OOXML du document correspond à une norme plus récente que "OoxmlComplianceCore.Ecma376".
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

Montre comment définir une spécification de conformité OOXML pour un document enregistré à respecter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour se conformer à Microsoft Word 2003,
// l'insertion d'une image définira sa forme à l'aide de VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML "ISO/IEC 29500:2008" ne prend pas en charge les formes VML.
// Si nous définissons la propriété "Compliance" de l'objet SaveOptions sur "OoxmlCompliance.Iso29500_2008_Strict",
 // tout document que nous enregistrons en passant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour respecter la norme OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


