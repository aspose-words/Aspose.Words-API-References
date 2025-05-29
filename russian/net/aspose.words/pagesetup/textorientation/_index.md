---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup TextOrientation, чтобы легко задать направление текста на странице. Настройте свой макет с параметрами, выходящими за рамки горизонтального расположения по умолчанию.
type: docs
weight: 430
url: /ru/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Позволяет указать`TextOrientation` для всей страницы. Значение по умолчанию:Horizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Примечания

Это свойство поддерживается только для собственных форматов MS Word: DOCX, WML, RTF и DOC.

## Примеры

Показывает, как задать ориентацию текста.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите свойство "TextOrientation" на "TextOrientation.Upward", чтобы повернуть весь текст на 90 градусов
// вправо, так что весь текст слева направо теперь будет идти сверху вниз.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Смотрите также

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
