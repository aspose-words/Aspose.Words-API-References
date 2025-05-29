---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase ScreenTip, улучшите пользовательский интерфейс, настроив текст подсказки, появляющейся при наведении мыши на фигуры.
type: docs
weight: 510
url: /ru/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Определяет текст, отображаемый при перемещении указателя мыши по фигуре.

```csharp
public string ScreenTip { get; set; }
```

## Примечания

Значение по умолчанию — пустая строка.

## Примеры

Показывает, как вставить фигуру, содержащую изображение, а также являющуюся гиперссылкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + щелчок левой кнопкой мыши по фигуре в Microsoft Word откроет новое окно веб-браузера
// и перенаправляем нас к гиперссылке в свойстве "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
