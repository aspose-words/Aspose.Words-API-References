---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.ShadowType per migliorare le tue forme con tipi di ombre personalizzabili per ottenere effetti visivi straordinari nei documenti.
type: docs
weight: 1630
url: /it/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Specifica il tipo di ombra di una forma.

```csharp
public enum ShadowType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ShadowMixed | `-2` | Nessuna delle impostazioni predefinite per le ombre. |
| Shadow1 | `1` | Primo tipo di ombra. |
| Shadow10 | `10` | Decimo tipo di ombra. |
| Shadow11 | `11` | Undicesimo tipo di ombra. |
| Shadow12 | `12` | Dodicesimo tipo di ombra. |
| Shadow13 | `13` | Tredicesimo tipo di ombra. |
| Shadow14 | `14` | Quattordicesimo tipo di ombra. |
| Shadow15 | `15` | Quindicesimo tipo di ombra. |
| Shadow16 | `16` | Sedicesimo tipo di ombra. |
| Shadow17 | `17` | Diciassettesimo tipo di ombra. |
| Shadow18 | `18` | Diciottesimo tipo di ombra. |
| Shadow19 | `19` | Diciannovesimo tipo di ombra. |
| Shadow2 | `2` | Secondo tipo di ombra. |
| Shadow20 | `20` | Ventesimo tipo di ombra. |
| Shadow21 | `21` | Ventunesimo tipo di ombra. |
| Shadow22 | `22` | Tipo di ombra di venti secondi. |
| Shadow23 | `23` | Ventitreesimo tipo di ombra. |
| Shadow24 | `24` | Ventiquattresimo tipo di ombra. |
| Shadow25 | `25` | Venticinquesimo tipo di ombra. |
| Shadow26 | `26` | Ventiseiesimo tipo di ombra. |
| Shadow27 | `27` | Ventisettesimo tipo di ombra. |
| Shadow28 | `28` | Ventottesimo tipo di ombra. |
| Shadow29 | `29` | Ventinovesimo tipo di ombra. |
| Shadow3 | `3` | Terzo tipo di ombra. |
| Shadow30 | `30` | Trentesimo tipo di ombra. |
| Shadow31 | `31` | Trentunesimo tipo di ombra. |
| Shadow32 | `32` | Tipo di ombra di trenta secondi. |
| Shadow33 | `33` | Trentatreesimo tipo di ombra. |
| Shadow34 | `34` | Trentaquattro tipi di ombra. |
| Shadow35 | `35` | Trentacinquesimo tipo di ombra. |
| Shadow36 | `36` | Trentaseiesimo tipo di ombra. |
| Shadow37 | `37` | Trentasettesimo tipo di ombra. |
| Shadow38 | `38` | Trentottesimo tipo di ombra. |
| Shadow39 | `39` | Trentanovesimo tipo di ombra. |
| Shadow4 | `4` | Quarto tipo di ombra. |
| Shadow40 | `40` | Quarantesimo tipo di ombra. |
| Shadow41 | `41` | Quarantunesimo tipo di ombra. |
| Shadow42 | `42` | Tipo di ombra di quaranta secondi. |
| Shadow43 | `43` | Quarantatreesimo tipo di ombra. |
| Shadow5 | `5` | Quinto tipo di ombra. |
| Shadow6 | `6` | Sesto tipo di ombra. |
| Shadow7 | `7` | Settimo tipo di ombra. |
| Shadow8 | `8` | Ottavo tipo di ombra. |
| Shadow9 | `9` | Nono tipo di ombra. |

## Osservazioni

ShadowType non è un semplice attributo, ma un preset che imposta contemporaneamente diversi attributi che formano l'aspetto dell'ombra.

## Esempi

Mostra come lavorare con una formattazione ombra per la forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
