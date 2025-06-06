---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words pour .NET
description: Gérez les cases à cocher SDT avec la propriété StructuredDocumentTag Checked. Obtenez et définissez facilement son état ; la valeur par défaut est « false ». Améliorez l'interactivité de vos documents dès aujourd'hui !
type: docs
weight: 60
url: /fr/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Obtient/Définit l'état actuel de la case à cocher**SDT** . La valeur par défaut de cette propriété est`FAUX` .

```csharp
public bool Checked { get; set; }
```

## Remarques

L'accès à cette propriété ne fonctionnera que pourCheckbox Types SDT.

Pour tous les autres types de SDT, une exception se produira.

## Exemples

Montrez comment créer une balise de document structurée sous la forme d'une case à cocher.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// Nous pouvons définir les symboles utilisés pour représenter l'état coché/décoché d'un contrôle de contenu de case à cocher.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
