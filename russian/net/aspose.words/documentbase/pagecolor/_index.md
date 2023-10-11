---
title: DocumentBase.PageColor
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBase свойство. Получает или задает цвет страницы документа. Это свойство представляет собой более простую версиюBackgroundShape .
type: docs
weight: 60
url: /ru/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Получает или задает цвет страницы документа. Это свойство представляет собой более простую версию[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

### Примечания

Это свойство обеспечивает простой способ указать сплошной цвет страницы для документа. Установка этого свойства создает и устанавливает соответствующий[`BackgroundShape`](../backgroundshape/).

Если цвет страницы не установлен (например, в документе нет фоновой фигуры), return Empty.

### Примеры

Показывает, как установить цвет фона для всех страниц документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Смотрите также

* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../documentbase/)
* сборка [Aspose.Words](../../../)


