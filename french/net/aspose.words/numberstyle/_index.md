---
title: NumberStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie le style de numérotation pour une liste les notes de bas de page et les notes de fin les numéros de page.
type: docs
weight: 4070
url: /fr/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Spécifie le style de numérotation pour une liste, les notes de bas de page et les notes de fin, les numéros de page.

```csharp
public enum NumberStyle
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Arabic | `0` | Numérotation arabe (1, 2, 3, ...) |
| UppercaseRoman | `1` | Majuscules romains (I, II, III, ...) |
| LowercaseRoman | `2` | Minuscule romain (i, ii, iii, ...) |
| UppercaseLetter | `3` | Lettre majuscule (A, B, C, ...) |
| LowercaseLetter | `4` | Lettre minuscule (a, b, c, ...) |
| Ordinal | `5` | Ordinal (1er, 2ème, 3ème, ...) |
| Number | `6` | Numéroté (Un, Deux, Trois, ...) |
| OrdinalText | `7` | Ordinal (texte) (Premier, Deuxième, Troisième, ...) |
| Hex | `8` | Hexadécimal : 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Manuel de style de Chicago : *, †, † |
| Kanji | `10` | Idéogramme-numérique |
| KanjiDigit | `11` | comptage japonais |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Arabe pleine chasse : 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Arabe demi-chasse : 1, 2, 3, 4 |
| KanjiTraditional | `16` | Juridique japonais |
| KanjiTraditional2 | `17` | Dix mille numériques japonais |
| NumberInCircle | `18` | Cercles fermés |
| DecimalFullWidth | `19` | Pleine largeur décimale : 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo pleine largeur |
| Iroha | `21` | Iroha pleine largeur |
| LeadingZero | `22` | Zéro non significatif (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Puce (vérifiez le code du caractère dans le texte) |
| Ganada | `24` | Coréen Ganada |
| Chosung | `25` | Corée Chosung |
| GB1 | `26` | Point ci-joint |
| GB2 | `27` | Parenthèses fermées |
| GB3 | `28` | Cercle fermé Chinois |
| GB4 | `29` | Idéogramme cercle fermé |
| Zodiac1 | `30` | Idéogramme traditionnel |
| Zodiac2 | `31` | Idéogramme Zodiaque |
| Zodiac3 | `32` | Idéogramme Zodiaque traditionnel |
| TradChinNum1 | `33` | comptage taiwanais |
| TradChinNum2 | `34` | Idéogramme légal traditionnel |
| TradChinNum3 | `35` | Taïwanais comptant mille |
| TradChinNum4 | `36` | numérique taïwanais |
| SimpChinNum1 | `37` | comptage chinois |
| SimpChinNum2 | `38` | Juridique chinois simplifié |
| SimpChinNum3 | `39` | Chinois comptant mille |
| SimpChinNum4 | `40` | chinois (non implémenté) |
| HanjaRead | `41` | numérique coréen |
| HanjaReadDigit | `42` | comptage coréen |
| Hangul | `43` | Corée legal |
| Hanja | `44` | Corée numérique2 |
| Hebrew1 | `45` | Hébreu-1 |
| Arabic1 | `46` | Arabe alpha |
| Hebrew2 | `47` | Hébreu-2 |
| Arabic2 | `48` | Arabe abjad |
| HindiLetter1 | `49` | Voyelles hindi |
| HindiLetter2 | `50` | consonnes hindi |
| HindiArabic | `51` | Numéros hindi |
| HindiCardinalText | `52` | Hindi descriptif (cardinaux) |
| ThaiLetter | `53` | Lettres thaïlandaises |
| ThaiArabic | `54` | Chiffres thaïlandais |
| ThaiCardinalText | `55` | Descriptif thaïlandais (cardinaux) |
| VietCardinalText | `56` | Descriptif vietnamien (cardinaux) |
| NumberInDash | `57` | Format du numéro de page : - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Alphabet russe minuscule |
| UppercaseRussian | `59` | Alphabet russe majuscule |
| None | `255` | Pas de puce ou de numéro. |
| Custom | `65280` | Format de nombre personnalisé. Il est pris en charge uniquement par le format DOCX. |

### Exemples

Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l'utilisation de DocumentBuilder.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation. 
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de document. 
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Crée une liste à partir d'un modèle Microsoft Word et personnalise les deux premiers de ses niveaux de liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Cette valeur NumberFormat créera des symboles de liste à puces en forme d'étoile.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Créez des paragraphes et appliquez-leur les deux niveaux de liste de notre formatage de liste personnalisé.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
