---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ListLevel GetEffectiveValue pour récupérer facilement les représentations sous forme de chaîne des éléments d'une liste. Personnalisez-la avec les options NumberStyle et Format !
type: docs
weight: 190
url: /fr/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Indique la représentation sous forme de chaîne de[`ListLevel`](../)objet pour l'index spécifié de l'élément de liste. Les paramètres spécifient[`NumberStyle`](../../../aspose.words/numberstyle/) et une chaîne de format facultative utilisée lorsqueCustom est spécifié.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | L'index de l'élément de la liste (doit être compris entre 1 et 32767). |
| numberStyle | NumberStyle | Le[`NumberStyle`](../../../aspose.words/numberstyle/) de la[`ListLevel`](../) objet. |
| customNumberStyleFormat | String | La chaîne de format facultative utilisée lorsqueCustom est spécifié (par exemple "a, ç, ĝ, ..."). Dans les autres cas, ce paramètre doit être`nul` ou vide. |

### Return_Value

La représentation sous forme de chaîne de[`ListLevel`](../) objet, décrit par le*numberStyle* paramètre and le*customNumberStyleFormat* paramètre, dans l'élément de liste à la position déterminée par le*index* paramètre.

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* est`nul` ou vide lorsque le*numberStyle* est personnalisé.-ou- *customNumberStyleFormat* n'est pas`nul` ou vide lorsque le*numberStyle* n'est pas personnalisé.-ou- *customNumberStyleFormat* est invalide. |
| ArgumentOutOfRangeException | l'index est hors de portée. |

## Exemples

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

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
