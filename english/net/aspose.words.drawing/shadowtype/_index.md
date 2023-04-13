---
title: ShadowType Enum
linktitle: ShadowType
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.ShadowType enum. Specifies the type of a shape shadow in C#.
type: docs
weight: 1130
url: /net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Specifies the type of a shape shadow.

```csharp
public enum ShadowType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| ShadowMixed | `-2` | None of predefined shadow presets. |
| Shadow1 | `1` | First shadow type. |
| Shadow10 | `10` | Tenth shadow type. |
| Shadow11 | `11` | Eleventh shadow type. |
| Shadow12 | `12` | Twelfth shadow type. |
| Shadow13 | `13` | Thirteenth shadow type. |
| Shadow14 | `14` | Fourteenth shadow type. |
| Shadow15 | `15` | Fifteenth shadow type. |
| Shadow16 | `16` | Sixteenth shadow type. |
| Shadow17 | `17` | Seventeenth shadow type. |
| Shadow18 | `18` | Eighteenth shadow type. |
| Shadow19 | `19` | Nineteenth shadow type. |
| Shadow2 | `2` | Second shadow type. |
| Shadow20 | `20` | Twentieth shadow type. |
| Shadow21 | `21` | Twenty first shadow type. |
| Shadow22 | `22` | Twenty second shadow type. |
| Shadow23 | `23` | Twenty third shadow type. |
| Shadow24 | `24` | Twenty forth shadow type. |
| Shadow25 | `25` | Twenty fifth shadow type. |
| Shadow26 | `26` | Twenty sixth shadow type. |
| Shadow27 | `27` | Twenty seventh shadow type. |
| Shadow28 | `28` | Twenty eighth shadow type. |
| Shadow29 | `29` | Twenty ninth shadow type. |
| Shadow3 | `3` | Third shadow type. |
| Shadow30 | `30` | Thirtieth shadow type. |
| Shadow31 | `31` | Thirty first shadow type. |
| Shadow32 | `32` | Thirty second shadow type. |
| Shadow33 | `33` | Thirty third shadow type. |
| Shadow34 | `34` | Thirty forth shadow type. |
| Shadow35 | `35` | Thirty fifth shadow type. |
| Shadow36 | `36` | Thirty sixth shadow type. |
| Shadow37 | `37` | Thirty seventh shadow type. |
| Shadow38 | `38` | Thirty eighth shadow type. |
| Shadow39 | `39` | Thirty ninth shadow type. |
| Shadow4 | `4` | Fourth shadow type. |
| Shadow40 | `40` | Fortieth shadow type. |
| Shadow41 | `41` | Forty first shadow type. |
| Shadow42 | `42` | Forty second shadow type. |
| Shadow43 | `43` | Forty third shadow type. |
| Shadow5 | `5` | Fifth shadow type. |
| Shadow6 | `6` | Sixth shadow type. |
| Shadow7 | `7` | Seventh shadow type. |
| Shadow8 | `8` | Eighth shadow type. |
| Shadow9 | `9` | Ninth shadow type. |

## Remarks

ShadowType is not a simple attribute, but a preset that sets at once several attributes which form the shadow appearance.

## Examples

Shows how to work with a shadow formatting for the shape.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
