---
title: StructuredDocumentTag.SetUncheckedSymbol
linktitle: SetUncheckedSymbol
articleTitle: SetUncheckedSymbol
second_title: Aspose.Words pour .NET
description: StructuredDocumentTag SetUncheckedSymbol méthode. Définit le symbole utilisé pour représenter létat non coché dun contrôle de contenu de case à cocher en C#.
type: docs
weight: 370
url: /fr/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Définit le symbole utilisé pour représenter l'état non coché d'un contrôle de contenu de case à cocher.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| characterCode | Int32 | Le code de caractère pour le symbole spécifié. |
| fontName | String | Nom de la police qui contient le symbole. |

## Remarques

L'accès à cette méthode ne fonctionnera que pourCheckbox Types SDT.

Pour tous les autres types de SDT, une exception se produira.

## Exemples

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

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
