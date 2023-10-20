---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words для .NET
description: PageSetup TextOrientation свойство. Позволяет указатьTextOrientation для всей страницы. Значение по умолчаниюHorizontal на С#.
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

Это свойство поддерживается только для собственных форматов MS Word DOCX, WML, RTF и DOC.

## Примеры

Показывает, как установить ориентацию текста.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите для свойства TextOrientation значение TextOrientation.Upward, чтобы повернуть весь текст на 90 градусов.
// вправо, так что весь текст слева направо теперь идет сверху вниз.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Смотрите также

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
