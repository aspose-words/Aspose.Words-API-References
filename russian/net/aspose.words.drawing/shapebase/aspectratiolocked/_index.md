---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase AspectRatioLocked, чтобы без усилий поддерживать соотношение сторон ваших фигур для идеальных дизайнов. Улучшите свои проекты сегодня!
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

Действует только для фигур верхнего уровня.

## Примеры

Показывает, как заблокировать/разблокировать соотношение сторон фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить фигуру. Если мы откроем этот документ в Microsoft Word, мы можем щелкнуть левой кнопкой мыши по фигуре, чтобы увидеть
// восемь маркеров размера по периметру, которые мы можем перетаскивать, чтобы изменить его размер.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Установите свойство "AspectRatioLocked" в значение "true", чтобы сохранить пропорции фигуры
// при использовании любого из четырех диагональных маркеров размера, которые изменяют как высоту, так и ширину изображения.
// Использование любых ортогональных маркеров размера, которые изменяют либо высоту, либо ширину, все равно приведет к изменению соотношения сторон.
// Установите свойство "AspectRatioLocked" в значение "false", чтобы разрешить нам
// свободно изменять соотношение сторон изображения с помощью всех маркеров размера.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
