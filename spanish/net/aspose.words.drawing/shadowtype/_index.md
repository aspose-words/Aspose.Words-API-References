---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.ShadowType enumeración. Especifica el tipo de sombra de forma en C#.
type: docs
weight: 1240
url: /es/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Especifica el tipo de sombra de forma.

```csharp
public enum ShadowType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| ShadowMixed | `-2` | Ninguno de los ajustes preestablecidos de sombra predefinidos. |
| Shadow1 | `1` | Primer tipo de sombra. |
| Shadow10 | `10` | Décimo tipo de sombra. |
| Shadow11 | `11` | Undécimo tipo de sombra. |
| Shadow12 | `12` | Duodécimo tipo de sombra. |
| Shadow13 | `13` | Decimotercer tipo de sombra. |
| Shadow14 | `14` | Decimocuarto tipo de sombra. |
| Shadow15 | `15` | Decimoquinto tipo de sombra. |
| Shadow16 | `16` | Decimosexto tipo de sombra. |
| Shadow17 | `17` | Decimoséptimo tipo de sombra. |
| Shadow18 | `18` | Decimoctavo tipo de sombra. |
| Shadow19 | `19` | Decimonoveno tipo de sombra. |
| Shadow2 | `2` | Segundo tipo de sombra. |
| Shadow20 | `20` | Vigésimo tipo de sombra. |
| Shadow21 | `21` | Vigésimo primer tipo de sombra. |
| Shadow22 | `22` | Tipo de sombra de veinte segundos. |
| Shadow23 | `23` | Vigésimo tercer tipo de sombra. |
| Shadow24 | `24` | Vigésimo cuarto tipo de sombra. |
| Shadow25 | `25` | Vigésimo quinto tipo de sombra. |
| Shadow26 | `26` | Vigésimo sexto tipo de sombra. |
| Shadow27 | `27` | Vigésimo séptimo tipo de sombra. |
| Shadow28 | `28` | Vigésimo octavo tipo de sombra. |
| Shadow29 | `29` | Vigésimo noveno tipo de sombra. |
| Shadow3 | `3` | Tercer tipo de sombra. |
| Shadow30 | `30` | Trigésimo tipo de sombra. |
| Shadow31 | `31` | Trigésimo primer tipo de sombra. |
| Shadow32 | `32` | Tipo de sombra de treinta segundos. |
| Shadow33 | `33` | Trigésimo tercer tipo de sombra. |
| Shadow34 | `34` | Treinta y cuatro tipo de sombra. |
| Shadow35 | `35` | Trigésimo quinto tipo de sombra. |
| Shadow36 | `36` | Trigésimo sexto tipo de sombra. |
| Shadow37 | `37` | Trigésimo séptimo tipo de sombra. |
| Shadow38 | `38` | Trigésimo octavo tipo de sombra. |
| Shadow39 | `39` | Trigésimo noveno tipo de sombra. |
| Shadow4 | `4` | Cuarto tipo de sombra. |
| Shadow40 | `40` | Cuadragésimo tipo de sombra. |
| Shadow41 | `41` | Cuadragésimo primer tipo de sombra. |
| Shadow42 | `42` | Tipo de sombra de cuarenta segundos. |
| Shadow43 | `43` | Cuadragésimo tercer tipo de sombra. |
| Shadow5 | `5` | Quinto tipo de sombra. |
| Shadow6 | `6` | Sexto tipo de sombra. |
| Shadow7 | `7` | Séptimo tipo de sombra. |
| Shadow8 | `8` | Octavo tipo de sombra. |
| Shadow9 | `9` | Noveno tipo de sombra. |

## Observaciones

ShadowType no es un atributo simple, sino un ajuste preestablecido que establece a la vez varios atributos que forman la apariencia de la sombra .

## Ejemplos

Muestra cómo trabajar con un formato de sombra para la forma.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
