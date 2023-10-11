---
title: StructuredDocumentTag.StructuredDocumentTag
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTag constructeur. Initialise une nouvelle instance du Balise de document structuré classe.
type: docs
weight: 10
url: /fr/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Initialise une nouvelle instance du **Balise de document structuré** classe.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |
| type | SdtType | Type de nœud SDT. |
| level | MarkupLevel | Niveau du nœud SDT dans le document. |

### Remarques

Les types de SDT suivants peuvent être créés :

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

### Exemples

Montrez comment créer une balise de document structuré sous la forme d'une case à cocher.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Nous pouvons définir les symboles utilisés pour représenter l'état coché/non coché d'un contrôle de contenu de case à cocher.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Voir également

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttag/)
* Assemblée [Aspose.Words](../../../)


