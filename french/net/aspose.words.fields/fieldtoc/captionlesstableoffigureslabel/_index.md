---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldToc CaptionlessTableOfFiguresLabel pour personnaliser votre table des figures. Gérez facilement les identifiants de séquence sans légende !
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Obtient ou définit le nom de l'identifiant de séquence utilisé lors de la création d'un tableau de figures qui n'inclut pas l'étiquette et le numéro de la légende .

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Exemples

Montre comment définir le nom de l'identifiant de séquence.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Voir également

* class [FieldToc](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
