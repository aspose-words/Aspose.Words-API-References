---
title: Enum ShadowType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.ShadowType enum. Specifica il tipo di ombra della forma.
type: docs
weight: 1240
url: /it/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Specifica il tipo di ombra della forma.

```csharp
public enum ShadowType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ShadowMixed | `-2` | Nessuna delle ombre predefinite predefinite. |
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
| Shadow22 | `22` | Tipo di ombra ventiduesimo. |
| Shadow23 | `23` | Ventitreesimo tipo di ombra. |
| Shadow24 | `24` | Ventiquattresimo tipo di ombra. |
| Shadow25 | `25` | Venticinquesimo tipo di ombra. |
| Shadow26 | `26` | Ventiseiesimo tipo di ombra. |
| Shadow27 | `27` | Ventisettesimo tipo di ombra. |
| Shadow28 | `28` | Ventottesimo tipo ombra. |
| Shadow29 | `29` | Ventinovesimo tipo ombra. |
| Shadow3 | `3` | Terzo tipo di ombra. |
| Shadow30 | `30` | Trentesimo tipo di ombra. |
| Shadow31 | `31` | Trentunesimo tipo di ombra. |
| Shadow32 | `32` | Trentaduesimo tipo di ombra. |
| Shadow33 | `33` | Trentatreesimo tipo di ombra. |
| Shadow34 | `34` | Trentaquattresimo tipo di ombra. |
| Shadow35 | `35` | Trentacinquesimo tipo di ombra. |
| Shadow36 | `36` | Trentaseiesimo tipo di ombra. |
| Shadow37 | `37` | Trentasettesimo tipo ombra. |
| Shadow38 | `38` | Trentottesimo tipo ombra. |
| Shadow39 | `39` | Trentanovesimo tipo ombra. |
| Shadow4 | `4` | Quarto tipo di ombra. |
| Shadow40 | `40` | Quarantesimo tipo di ombra. |
| Shadow41 | `41` | Quarantunesimo tipo di ombra. |
| Shadow42 | `42` | Quarantaduesimo tipo di ombra. |
| Shadow43 | `43` | Quarantatreesimo tipo di ombra. |
| Shadow5 | `5` | Quinto tipo di ombra. |
| Shadow6 | `6` | Sesto tipo di ombra. |
| Shadow7 | `7` | Settimo tipo di ombra. |
| Shadow8 | `8` | Ottavo tipo di ombra. |
| Shadow9 | `9` | Nono tipo di ombra. |

### Osservazioni

ShadowType non è un semplice attributo, ma un preset che imposta contemporaneamente diversi attributi che formano l'aspetto dell'ombra.

### Esempi

Mostra come utilizzare la formattazione dell'ombra per la forma.

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


