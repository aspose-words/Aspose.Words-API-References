---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words для .NET
description: ShapeBase AspectRatioLocked свойство. Указывает заблокировано ли соотношение сторон фигуры на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Указывает, заблокировано ли соотношение сторон фигуры.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Примечания

Значение по умолчанию зависит от[`ShapeType`](../../shapetype/) , дляImage это`истинный` , но для других типов фигур это`ЛОЖЬ`.

Имеет эффект только для фигур верхнего уровня.

## Примеры

Показывает, как заблокировать/разблокировать соотношение сторон фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем фигуру. Если мы откроем этот документ в Microsoft Word, мы сможем щелкнуть левой кнопкой мыши по фигуре, чтобы открыть ее.
// восемь маркеров изменения размера по периметру, которые можно щелкнуть и перетащить, чтобы изменить размер.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Установите для свойства «AspectRatioLocked» значение «true», чтобы сохранить соотношение сторон фигуры
// при использовании любого из четырех диагональных маркеров изменения размера, которые изменяют как высоту, так и ширину изображения.
// Использование любых ортогональных маркеров размера, которые изменяют высоту или ширину, все равно приведет к изменению соотношения сторон.
// Установите для свойства «AspectRatioLocked» значение «false», чтобы мы могли
// свободно изменять соотношение сторон изображения с помощью всех маркеров размера.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
