---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.ShadowType opsomming. Gibt den Typ eines Formschattens an in C#.
type: docs
weight: 1240
url: /de/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Gibt den Typ eines Formschattens an.

```csharp
public enum ShadowType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| ShadowMixed | `-2` | Keine der vordefinierten Schattenvoreinstellungen. |
| Shadow1 | `1` | Erster Schattentyp. |
| Shadow10 | `10` | Zehnter Schattentyp. |
| Shadow11 | `11` | Elfter Schattentyp. |
| Shadow12 | `12` | Zwölfter Schattentyp. |
| Shadow13 | `13` | Dreizehnter Schattentyp. |
| Shadow14 | `14` | Vierzehnter Schattentyp. |
| Shadow15 | `15` | Fünfzehnter Schattentyp. |
| Shadow16 | `16` | Sechzehnter Schattentyp. |
| Shadow17 | `17` | Siebzehnter Schattentyp. |
| Shadow18 | `18` | Achtzehnter Schattentyp. |
| Shadow19 | `19` | Neunzehnter Schattentyp. |
| Shadow2 | `2` | Zweiter Schattentyp. |
| Shadow20 | `20` | Zwanzigster Schattentyp. |
| Shadow21 | `21` | Einundzwanzigster Schattentyp. |
| Shadow22 | `22` | Zwanzig-Sekunden-Schattentyp. |
| Shadow23 | `23` | Dreiundzwanzigster Schattentyp. |
| Shadow24 | `24` | Vierundzwanzigster Schattentyp. |
| Shadow25 | `25` | Fünfundzwanzigster Schattentyp. |
| Shadow26 | `26` | Sechsundzwanzigster Schattentyp. |
| Shadow27 | `27` | Siebenundzwanzigster Schattentyp. |
| Shadow28 | `28` | Achtundzwanzigster Schattentyp. |
| Shadow29 | `29` | Neunundzwanzigster Schattentyp. |
| Shadow3 | `3` | Dritter Schattentyp. |
| Shadow30 | `30` | Dreißigster Schattentyp. |
| Shadow31 | `31` | Einunddreißigster Schattentyp. |
| Shadow32 | `32` | Zweiunddreißigster Schattentyp. |
| Shadow33 | `33` | Dreiunddreißigster Schattentyp. |
| Shadow34 | `34` | Dreißigster Schattentyp. |
| Shadow35 | `35` | Fünfunddreißigster Schattentyp. |
| Shadow36 | `36` | Sechsunddreißigster Schattentyp. |
| Shadow37 | `37` | Siebenunddreißigster Schattentyp. |
| Shadow38 | `38` | Achtunddreißigster Schattentyp. |
| Shadow39 | `39` | Neununddreißigster Schattentyp. |
| Shadow4 | `4` | Vierter Schattentyp. |
| Shadow40 | `40` | Vierzigster Schattentyp. |
| Shadow41 | `41` | Einundvierzigster Schattentyp. |
| Shadow42 | `42` | Zweiundvierzigster Schattentyp. |
| Shadow43 | `43` | Dreiundvierzigster Schattentyp. |
| Shadow5 | `5` | Fünfter Schattentyp. |
| Shadow6 | `6` | Sechster Schattentyp. |
| Shadow7 | `7` | Siebter Schattentyp. |
| Shadow8 | `8` | Achter Schattentyp. |
| Shadow9 | `9` | Neunter Schattentyp. |

## Bemerkungen

ShadowType ist kein einfaches Attribut, sondern eine Voreinstellung, die mehrere Attribute gleichzeitig festlegt, die das Erscheinungsbild des Schattens bilden.

## Beispiele

Zeigt, wie mit einer Schattenformatierung für die Form gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
