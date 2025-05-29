---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentBase PageColor, чтобы легко настроить цвет страницы вашего документа. Упростите дизайн с помощью этой удобной функции!
type: docs
weight: 70
url: /ru/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Возвращает или задает цвет страницы документа. Это свойство является более простой версией[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Примечания

Это свойство обеспечивает простой способ указать сплошной цвет страницы для документа. Установка этого свойства создает и задает соответствующий[`BackgroundShape`](../backgroundshape/).

Если цвет страницы не установлен (например, в документе отсутствует фоновая фигура), возвращается Empty.

## Примеры

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
