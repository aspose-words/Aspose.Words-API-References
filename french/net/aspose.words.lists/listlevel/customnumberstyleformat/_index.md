---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words pour .NET
description: ListLevel CustomNumberStyleFormat propriété. Obtient le format de style de numéro personnalisé pour ce niveau de liste. Par exemple  a ç ĝ  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Obtient le format de style de numéro personnalisé pour ce niveau de liste. Par exemple : "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; }
```

## Exemples

Montre comment obtenir le format d’une liste avec le style de numéro personnalisé.

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
