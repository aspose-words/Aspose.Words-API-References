---
title: ShapeBase.ScreenTip
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Определяет текст отображаемый при наведении указателя мыши на фигуру.
type: docs
weight: 480
url: /ru/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Определяет текст, отображаемый при наведении указателя мыши на фигуру.

```csharp
public string ScreenTip { get; set; }
```

### Примечания

Значение по умолчанию — пустая строка.

### Примеры

Показывает, как вставить фигуру, содержащую изображение, а также гиперссылку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + щелчок левой кнопкой мыши по фигуре в Microsoft Word откроет новое окно веб-браузера
// и приведет нас к гиперссылке в свойстве "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


