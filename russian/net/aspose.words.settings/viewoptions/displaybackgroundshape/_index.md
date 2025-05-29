---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DisplayBackgroundShape в ViewOptions, чтобы улучшить макет печати с помощью настраиваемых фоновых фигур для придания ему изысканного вида.
type: docs
weight: 10
url: /ru/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Управляет отображением фоновой формы в режиме макета печати.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## Примеры

Показывает, как скрыть/отобразить фоновые изображения документа в параметрах просмотра.

```csharp
// Используйте HTML-строку для создания нового документа с однотонным фоновым цветом.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// Исходный документ имеет однотонный цветной фон,
// наличие которого установит флаг "DisplayBackgroundShape" в значение "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Оставьте «DisplayBackgroundShape» равным «true», чтобы документ отображал цвет фона.
// Это может повлиять на некоторые цвета текста для улучшения видимости.
// Установите для «DisplayBackgroundShape» значение «false», чтобы не отображать цвет фона.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Смотрите также

* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
