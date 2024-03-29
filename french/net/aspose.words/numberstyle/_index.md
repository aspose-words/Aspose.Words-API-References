---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words pour .NET
description: Aspose.Words.NumberStyle énumération. Spécifie le style de numérotation dune liste les notes de bas de page et de fin les numéros de page en C#.
type: docs
weight: 4310
url: /fr/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Spécifie le style de numérotation d'une liste, les notes de bas de page et de fin, les numéros de page.

```csharp
public enum NumberStyle
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Arabic | `0` | Numérotation arabe (1, 2, 3, ...) |
| UppercaseRoman | `1` | Majuscules romaines (I, II, III, ...) |
| LowercaseRoman | `2` | Minuscules romains (i, ii, iii, ...) |
| UppercaseLetter | `3` | Lettre majuscule (A, B, C, ...) |
| LowercaseLetter | `4` | Lettre minuscule (a, b, c, ...) |
| Ordinal | `5` | Ordinal (1er, 2e, 3e, ...) |
| Number | `6` | Numéroté (Un, Deux, Trois, ...) |
| OrdinalText | `7` | Ordinal (texte) (Premier, Deuxième, Troisième, ...) |
| Hex | `8` | Hexadécimal : 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Manuel de style de Chicago : *, †, † |
| Kanji | `10` | Idéographe-digital |
| KanjiDigit | `11` | comptage japonais |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Arabe pleine largeur : 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Arabe demi-chasse : 1, 2, 3, 4 |
| KanjiTraditional | `16` | Légal japonais |
| KanjiTraditional2 | `17` | Dix mille numériques japonais |
| NumberInCircle | `18` | Cercles fermés |
| DecimalFullWidth | `19` | Décimal pleine largeur : 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo pleine largeur |
| Iroha | `21` | Iroha pleine largeur |
| LeadingZero | `22` | Zéro initial (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Bullet (vérifiez le code du caractère dans le texte) |
| Ganada | `24` | Coréen Ganada |
| Chosung | `25` | Corée Chosung |
| GB1 | `26` | Point final fermé |
| GB2 | `27` | Parenthèse fermée |
| GB3 | `28` | Cercle fermé Chinese |
| GB4 | `29` | Idéogramme cercle fermé |
| Zodiac1 | `30` | Idéogramme traditionnel |
| Zodiac2 | `31` | Idéogramme Zodiaque |
| Zodiac3 | `32` | Idéogramme du zodiaque traditionnel |
| TradChinNum1 | `33` | Comptage taïwanais |
| TradChinNum2 | `34` | Idéogramme légal traditionnel |
| TradChinNum3 | `35` | Taïwanais comptant des milliers |
| TradChinNum4 | `36` | numérique taïwanais |
| SimpChinNum1 | `37` | Comptage chinois |
| SimpChinNum2 | `38` | Juridique chinois simplifié |
| SimpChinNum3 | `39` | Chinois comptant des milliers |
| SimpChinNum4 | `40` | Chinois (non implémenté) |
| HanjaRead | `41` | coréen numérique |
| HanjaReadDigit | `42` | Comptage coréen |
| Hangul | `43` | Corée légal |
| Hanja | `44` | Corée digital2 |
| Hebrew1 | `45` | Hébreu-1 |
| Arabic1 | `46` | arabe alpha |
| Hebrew2 | `47` | Hébreu-2 |
| Arabic2 | `48` | arabe abjad |
| HindiLetter1 | `49` | Voyelles hindi |
| HindiLetter2 | `50` | Consonnes hindi |
| HindiArabic | `51` | Numéros hindi |
| HindiCardinalText | `52` | Descriptif hindi (cardinaux) |
| ThaiLetter | `53` | Lettres thaïlandaises |
| ThaiArabic | `54` | Numéros thaïlandais |
| ThaiCardinalText | `55` | Descriptif thaïlandais (cardinaux) |
| VietCardinalText | `56` | Descriptif vietnamien (cardinaux) |
| NumberInDash | `57` | Format du numéro de page : - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Alphabet russe minuscule |
| UppercaseRussian | `59` | Alphabet russe majuscule |
| None | `255` | Pas de puce ni de numéro. |
| Custom | `65280` | Format de numéro personnalisé. Il est pris en charge uniquement par le format DOCX. |

## Exemples

Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l’utilisation de DocumentBuilder.

```csharp
Document doc = new Document();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
 // Nous pouvons créer des listes imbriquées en augmentant le niveau d'indentation.
 // Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un générateur de documents.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d'un modèle Microsoft Word et personnalisez les deux premiers niveaux de liste.
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
