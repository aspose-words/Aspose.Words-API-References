---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fields.GeneralFormat, qui améliore la mise en forme du texte numérique pour les champs, garantissant clarté et précision dans vos documents.
type: docs
weight: 3050
url: /fr/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Spécifie un format général qui est appliqué à un résultat numérique, textuel ou à tout résultat de champ. Un champ peut avoir une combinaison de formats généraux.

```csharp
public enum GeneralFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Utilisé pour spécifier un format général manquant. |
| Aiueo | `1` | Formatage numérique. Formate un résultat numérique en utilisant les caractères hiragana dans l'ordre aiueo traditionnel. |
| UppercaseAlphabetic | `2` | Formatage numérique. Formate un résultat numérique comme une ou plusieurs occurrences d'un caractère alphabétique latin majuscule. |
| LowercaseAlphabetic | `3` | Formatage numérique. Formate un résultat numérique sous la forme d'une ou plusieurs occurrences d'un caractère alphabétique latin minuscule. |
| Arabic | `4` | Formatage numérique. Formate un résultat numérique en chiffres cardinaux arabes. |
| ArabicAbjad | `5` | Formatage numérique. Formate un résultat numérique en utilisant des nombres Abjad croissants. |
| ArabicAlpha | `6` | Formatage numérique. Formate un résultat numérique à l'aide de caractères de l'alphabet arabe. |
| ArabicDash | `7` | Formatage numérique. Formate un résultat numérique en chiffres arabes cardinaux, avec un préfixe « - » et un suffixe « - ». |
| BahtText | `8` | Formatage numérique. Formate un résultat numérique selon le système de comptage thaïlandais. |
| CardText | `9` | Formatage numérique. Texte cardinal (Un, Deux, Trois, ...). |
| ChineseNum1 | `10` | Formatage numérique. Formate un résultat numérique en utilisant les nombres croissants du système de comptage approprié. |
| ChineseNum2 | `11` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels conformes au format légal approprié. |
| ChineseNum3 | `12` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage des milliers approprié. |
| Chosung | `13` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du format coréen Chosung. |
| CircleNum | `14` | Formatage numérique. Formate un résultat numérique en utilisant une numérotation décimale entourée d'un cercle, en utilisant le caractère alphanumérique entouré pour les nombres compris entre 1 et 20. |
| DBChar | `15` | Formatage numérique. Formate un résultat numérique en utilisant la numérotation arabe sur deux octets. |
| DBNum1 | `16` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes numériques séquentiels, en utilisant le caractère approprié. |
| DBNum2 | `17` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage approprié. |
| DBNum3 | `18` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage légal approprié. |
| DBNum4 | `19` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels issus du système de comptage numérique approprié. |
| DollarText | `20` | Formatage numérique. Texte en dollars (Un, Deux, Trois, ... + ET 55/100). |
| Ganada | `21` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du format coréen Ganada. |
| GB1 | `22` | Formatage numérique. Formate un résultat numérique en utilisant une numérotation décimale suivie d'un point, en utilisant le caractère alphanumérique inclus. |
| GB2 | `23` | Formatage numérique. Formate un résultat numérique en utilisant une numérotation décimale entre parenthèses, et le caractère alphanumérique inclus. |
| GB3 | `24` | Formatage numérique. Formate un résultat numérique en utilisant une numérotation décimale entourée d'un cercle, à l'aide du caractère alphanumérique entouré. |
| GB4 | `25` | Formatage numérique. Formate un résultat numérique en utilisant une numérotation décimale entourée d'un cercle, à l'aide du caractère alphanumérique entouré. |
| Hebrew1 | `26` | Formatage numérique. Formate un résultat numérique en chiffres hébreux. |
| Hebrew2 | `27` | Formatage numérique. Formate un résultat numérique en utilisant l'alphabet hébreu. |
| Hex | `28` | Formatage numérique. Formate le résultat numérique en chiffres hexadécimaux majuscules. |
| HindiArabic | `29` | Formatage numérique. Formate un résultat numérique en utilisant des nombres hindi. |
| HindiCardText | `30` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage hindi. |
| HindiLetter1 | `31` | Formatage numérique. Formate un résultat numérique en utilisant les voyelles hindi. |
| HindiLetter2 | `32` | Formatage numérique. Formate un résultat numérique à l'aide des consonnes hindi. |
| Iroha | `33` | Formatage numérique. Formate un résultat numérique avec l'iroha japonais. |
| KanjiNum1 | `34` | Formatage numérique. Formate un résultat numérique selon un style japonais et le système de comptage approprié. |
| KanjiNum2 | `35` | Formatage numérique. Formate un résultat numérique selon le système de comptage approprié. |
| KanjiNum3 | `36` | Formatage numérique. Formate un résultat numérique selon le système de comptage approprié. |
| Ordinal | `37` | Formatage numérique. Ordinal (1er, 2e, 3e, ...). |
| OrdText | `38` | Formatage numérique. Texte ordinal (premier, deuxième, troisième, etc.). |
| UppercaseRoman | `39` | Formatage numérique. Majuscules romaines (I, II, III, ...). |
| LowercaseRoman | `40` | Formatage numérique. Minuscules romaines (i, ii, iii, ...). |
| SBChar | `41` | Formatage numérique. Formate un résultat numérique en utilisant la numérotation arabe sur un octet. |
| ThaiArabic | `42` | Formatage numérique. Formate un résultat numérique en utilisant des nombres thaïlandais. |
| ThaiCardText | `43` | Formatage numérique. Formate un résultat numérique à l'aide de nombres séquentiels du système de comptage thaïlandais. |
| ThaiLetter | `44` | Formatage numérique. Formate un résultat numérique en utilisant des lettres thaïlandaises. |
| VietCardText | `45` | Formatage numérique. Formate un résultat numérique en chiffres vietnamiens. |
| Zodiac1 | `46` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes numériques traditionnels séquentiels. |
| Zodiac2 | `47` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes zodiacaux séquentiels. |
| Zodiac3 | `48` | Formatage numérique. Formate un résultat numérique à l'aide d'idéogrammes zodiacaux traditionnels séquentiels. |
| Caps | `49` | Formatage du texte. La première lettre de chaque mot est en majuscule. |
| FirstCap | `50` | Formatage du texte. La première lettre du premier mot est en majuscule. |
| Lower | `51` | Formatage du texte. Toutes les lettres sont en minuscules. |
| Upper | `52` | Formatage du texte. Toutes les lettres sont en majuscules. |
| CharFormat | `53` | Formatage du résultat du champ. Instruction CHARFORMAT. |
| MergeFormat | `54` | Formatage du résultat du champ. Instruction MERGEFORMAT. |
| MergeFormatInet | `55` | Formatage du résultat du champ. Instruction MERGEFORMATINET. |

## Exemples

Montre comment formater les résultats des champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un générateur de documents pour insérer un champ qui affiche un résultat sans format appliqué.
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

// Nous pouvons supprimer nos formats pour ramener le résultat du champ à sa forme d'origine.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
