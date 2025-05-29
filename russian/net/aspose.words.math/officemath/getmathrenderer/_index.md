---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetMathRenderer от OfficeMath, позволяющий легко преобразовывать уравнения в изображения, улучшая ваши документы с помощью четких профессиональных визуальных эффектов.
type: docs
weight: 90
url: /ru/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Создает и возвращает объект, который можно использовать для преобразования этого уравнения в изображение.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Возвращаемое значение

Объект рендеринга для этого уравнения.

## Примечания

Этот метод просто вызывает[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) конструктор и передает этот объект в качестве параметра.

## Примеры

Показывает, как преобразовать объект Office Math в файл изображения в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Создаем объект "ImageSaveOptions" для передачи в метод "Save" рендерера узла для изменения
// как он преобразует узел OfficeMath в изображение.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Установите свойство «Масштаб» на 5, чтобы отрисовать объект в пять раз больше его исходного размера.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Смотрите также

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../../aspose.words.math/)
* сборка [Aspose.Words](../../../)
