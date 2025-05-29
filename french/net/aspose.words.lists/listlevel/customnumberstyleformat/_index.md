---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words pour .NET
description: Personnalisez vos niveaux de liste avec la propriété ListLevel CustomNumberStyleFormat. Définissez facilement des formats de nombres uniques pour un style de document amélioré.
type: docs
weight: 20
url: /fr/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Récupère ou définit le format de style de nombre personnalisé pour ce niveau de liste. Par exemple : « a, ç, ĝ, ... ».

```csharp
public string CustomNumberStyleFormat { get; set; }
```

## Exemples

Montre comment définir le format du style du numéro de client.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

doc.UpdateListLabels();

ParagraphCollection paras = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("0001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("0002.", paras[2].ListLabel.LabelString);

paras[1].ListFormat.ListLevel.CustomNumberStyleFormat = "001, 002, 003, ...";

doc.UpdateListLabels();

Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("002.", paras[2].ListLabel.LabelString);
```

Montre comment obtenir le format d'une liste avec le style de numéro personnalisé.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Nous pouvons obtenir la valeur de l'index spécifié de l'élément de liste.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Voir également

* class [ListLevel](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
