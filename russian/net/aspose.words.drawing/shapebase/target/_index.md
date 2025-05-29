---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Target, чтобы легко устанавливать или извлекать целевые рамки гиперссылок для ваших фигур, улучшая навигацию и взаимодействие с пользователем.
type: docs
weight: 560
url: /ru/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Получает или задает целевой фрейм для гиперссылки формы.

```csharp
public string Target { get; set; }
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
