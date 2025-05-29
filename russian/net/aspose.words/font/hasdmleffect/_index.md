---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words для .NET
description: Узнайте, применяется ли определенный текстовый эффект DrawingML с помощью метода Font HasDmlEffect. Улучшите визуальную привлекательность вашего документа без усилий!
type: docs
weight: 570
url: /ru/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Проверяет, применен ли определенный текстовый эффект DrawingML.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | Тип текстового эффекта DrawingML. |

### Возвращаемое значение

`истинный` если применен определенный текстовый эффект DrawingML.

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

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
