---
title: GeneralFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie un format général appliqué à un résultat numérique textuel ou à nimporte quel champ. Un champ peut avoir une combinaison de formats généraux.
type: docs
weight: 2480
url: /fr/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Spécifie un format général appliqué à un résultat numérique, textuel ou à n'importe quel champ. Un champ peut avoir une combinaison de formats généraux.

```csharp
public enum GeneralFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Utilisé pour spécifier un format général manquant. |
| Aiueo | `1` | Formatage numérique. Formate un résultat numérique en utilisant des caractères hiragana dans l'ordre aiueo traditionnel. |
| UppercaseAlphabetic | `2` | Formatage numérique. Formate un résultat numérique comme une ou plusieurs occurrences d'un caractère latin alphabétique majuscule. |
| LowercaseAlphabetic | `3` | Formatage numérique. Formate un résultat numérique comme une ou plusieurs occurrences d'un caractère latin alphabétique minuscule. |
| Arabic | `4` | Formatage numérique. Formate un résultat numérique à l'aide de chiffres cardinaux arabes. |
| ArabicAbjad | `5` | Formatage numérique. Formate un résultat numérique en utilisant des chiffres Abjad croissants. |
| ArabicAlpha | `6` | Formatage numérique. Formate un résultat numérique à l'aide de caractères de l'alphabet arabe. |
| ArabicDash | `7` | Formatage numérique. Formate un résultat numérique à l'aide de chiffres cardinaux arabes, avec un préfixe de "-" et un suffixe de " -". |
| BahtText | `8` | Formatage numérique. Formate un résultat numérique dans le système de comptage thaïlandais. |
| CardText | `9` | Formatage numérique. Texte cardinal (Un, Deux, Trois, ...). |
| ChineseNum1 | `10` | Formatage numérique. Formate un résultat numérique en utilisant les nombres croissants du système de comptage approprié. |
| ChineseNum2 | `11` | Formatage numérique. Formate un résultat numérique à l'aide de numéros séquentiels du format légal approprié. |
| ChineseNum3 | `12` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage des milliers approprié. |
| Chosung | `13` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du format coréen Chosung. |
| CircleNum | `14` | Formatage numérique. Formate un résultat numérique à l'aide d'une numérotation décimale entourée d'un cercle, en utilisant le caractère de glyphe alphanumérique entouré pour les nombres compris entre 1 et 20. |
| DBChar | `15` | Formatage numérique. Formate un résultat numérique à l'aide d'une numérotation arabe à deux octets. |
| DBNum1 | `16` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes numériques séquentiels, en utilisant le caractère approprié. |
| DBNum2 | `17` | Formatage numérique. Formate un résultat numérique en utilisant des nombres séquentiels du système de comptage approprié. |
| DBNum3 | `18` | Formatage numérique. Formate un résultat numérique à l'aide de numéros séquentiels du système de comptage légal approprié. |
| DBNum4 | `19` | Formatage numérique. Formate un résultat numérique à l'aide de numéros séquentiels du système de comptage numérique approprié. |
| DollarText | `20` | Formatage numérique. Texte en dollars (Un, Deux, Trois, ... + ET 55/100). |
| Ganada | `21` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du format coréen Ganada. |
| GB1 | `22` | Formatage numérique. Formate un résultat numérique en utilisant une numérotation décimale suivie d'un point, en utilisant le caractère de glyphe alphanumérique inclus. |
| GB2 | `23` | Formatage numérique. Formate un résultat numérique en utilisant la numérotation décimale entre parenthèses, en utilisant le caractère de glyphe alphanumérique entre parenthèses. |
| GB3 | `24` | Formatage numérique. Formate un résultat numérique à l'aide d'une numérotation décimale entourée d'un cercle, en utilisant le caractère de glyphe alphanumérique enfermé . |
| GB4 | `25` | Formatage numérique. Formate un résultat numérique à l'aide d'une numérotation décimale entourée d'un cercle, en utilisant le caractère de glyphe alphanumérique enfermé . |
| Hebrew1 | `26` | Formatage numérique. Formate un résultat numérique à l'aide de chiffres hébreux. |
| Hebrew2 | `27` | Formatage numérique. Formate un résultat numérique en utilisant l'alphabet hébreu. |
| Hex | `28` | Formatage numérique. Formate le résultat numérique en utilisant des chiffres hexadécimaux majuscules. |
| HindiArabic | `29` | Formatage numérique. Formate un résultat numérique à l'aide de nombres hindi. |
| HindiCardText | `30` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage hindi. |
| HindiLetter1 | `31` | Formatage numérique. Formate un résultat numérique à l'aide de voyelles hindi. |
| HindiLetter2 | `32` | Formatage numérique. Formate un résultat numérique à l'aide de consonnes hindi. |
| Iroha | `33` | Formatage numérique. Formate un résultat numérique en utilisant le japonais iroha. |
| KanjiNum1 | `34` | Formatage numérique. Formate un résultat numérique en utilisant un style japonais en utilisant le système de comptage approprié. |
| KanjiNum2 | `35` | Formatage numérique. Formate un résultat numérique en utilisant le système de comptage approprié. |
| KanjiNum3 | `36` | Formatage numérique. Formate un résultat numérique en utilisant le système de comptage approprié. |
| Ordinal | `37` | Formatage numérique. Ordinal (1er, 2ème, 3ème, ...). |
| OrdText | `38` | Formatage numérique. Texte ordinal (Premier, Deuxième, Troisième, ...). |
| UppercaseRoman | `39` | Formatage numérique. Majuscules romaines (I, II, III, ...). |
| LowercaseRoman | `40` | Formatage numérique. Minuscules romains (i, ii, iii, ...). |
| SBChar | `41` | Formatage numérique. Formate un résultat numérique à l'aide d'une numérotation arabe à un octet. |
| ThaiArabic | `42` | Formatage numérique. Formate un résultat numérique à l'aide de nombres thaïlandais. |
| ThaiCardText | `43` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage thaïlandais. |
| ThaiLetter | `44` | Formatage numérique. Formate un résultat numérique à l'aide de lettres thaïlandaises. |
| VietCardText | `45` | Formatage numérique. Formate un résultat numérique à l'aide de chiffres vietnamiens. |
| Zodiac1 | `46` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes numériques séquentiels traditionnels. |
| Zodiac2 | `47` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes séquentiels du zodiaque. |
| Zodiac3 | `48` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes traditionnels séquentiels du zodiaque. |
| Caps | `49` | Formatage du texte. Met en majuscule la première lettre de chaque mot. |
| FirstCap | `50` | Formatage du texte. Met en majuscule la première lettre du premier mot. |
| Lower | `51` | Formatage du texte. Toutes les lettres sont en minuscules. |
| Upper | `52` | Formatage du texte. Toutes les lettres sont en majuscules. |
| CharFormat | `53` | Formatage des résultats de champ. L'instruction CHARFORMAT. |
| MergeFormat | `54` | Formatage des résultats de champ. L'instruction MERGEFORMAT. |
| MergeFormatInet | `55` | Formatage des résultats de champ. L'instruction MERGEFORMATINET. |

### Exemples

Montre comment formater les résultats de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de document pour insérer un champ qui affiche un résultat sans format appliqué.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Nous pouvons appliquer un format au résultat d'un champ en utilisant les propriétés du champ.
// Vous trouverez ci-dessous trois types de formats que nous pouvons appliquer au résultat d'un champ.
// 1 - Format numérique :
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Format date/heure :
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Format général :
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Nous pouvons supprimer nos formats pour rétablir le résultat du champ dans sa forme d'origine.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
