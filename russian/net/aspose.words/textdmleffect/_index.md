---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.TextDmlEffect для улучшения текстовых последовательностей с помощью динамических эффектов DML. Улучшите презентацию вашего документа без усилий!
type: docs
weight: 7260
url: /ru/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Текстовый эффект Dml для текстовых последовательностей.

```csharp
public enum TextDmlEffect
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Glow | `0` | Эффект свечения, при котором за краями объекта добавляется цветной размытый контур. |
| Fill | `1` | Эффект наложения заливки. |
| Shadow | `2` | Эффект тени. |
| Outline | `3` | Эффект контура. |
| Effect3D | `4` | 3D эффект. |
| Reflection | `5` | Эффект отражения. |

## Примеры

Показывает, как проверить, отображает ли прогон текстовый эффект DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
