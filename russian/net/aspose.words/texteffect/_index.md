---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words для .NET
description: Исследуйте перечисление Aspose.Words.TextEffect для динамической текстовой анимации. Улучшите свои документы с помощью привлекательных эффектов для захватывающего пользовательского опыта.
type: docs
weight: 7270
url: /ru/net/aspose.words/texteffect/
---
## TextEffect enumeration

Эффект анимации для текста.

```csharp
public enum TextEffect
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## Примеры

Показывает, как применить визуальный эффект к прогону.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Старые версии Microsoft Word поддерживают только эффекты анимации шрифтов.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
