---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.ShapeMarkupLanguage énumération. Spécifie le langage de balisage utilisé pour la forme en C#.
type: docs
weight: 1280
url: /fr/net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Spécifie le langage de balisage utilisé pour la forme.

```csharp
public enum ShapeMarkupLanguage : byte
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Dml | `0` | Drawing Markup Language est utilisé pour définir la forme. |
| Vml | `1` | Vector Markup Language est utilisé pour définir la forme. |

## Exemples

Montre comment définir une spécification de conformité OOXML à laquelle un document enregistré doit adhérer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour se conformer à Microsoft Word 2003,
// l'insertion d'une image définira sa forme en utilisant VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML "ISO/IEC 29500:2008" ne prend pas en charge les formes VML.
// Si on fixe la propriété "Compliance" de l'objet SaveOptions à "OoxmlCompliance.Iso29500_2008_Strict",
 // tout document que nous enregistrons en transmettant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour adhérer à la norme OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
