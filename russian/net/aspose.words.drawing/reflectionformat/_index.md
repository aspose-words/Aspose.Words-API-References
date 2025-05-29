---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.ReflectionFormat для расширенного форматирования отражения объектов. Улучшите дизайн вашего документа с помощью бесшовной интеграции!
type: docs
weight: 1570
url: /ru/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Представляет форматирование отражения для объекта.

```csharp
public class ReflectionFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Возвращает или задает двойное значение, которое указывает степень эффекта размытия, применяемого к эффекту отражения в точках. Значение по умолчанию — 0.0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Возвращает или задает двойное значение, которое указывает величину разделения отраженного изображения от объекта в точках. Значение по умолчанию — 0.0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Возвращает или задает двойное значение от 0,0 до 1,0, представляющее размер отражения в процентах от отраженного объекта. Значение по умолчанию — 0,0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Возвращает или задает двойное значение от 0,0 (непрозрачный) до 1,0 (прозрачный), представляющее степень прозрачности для эффекта отражения. Значение по умолчанию — 0.0. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Удаляет`ReflectionFormat` из родительского объекта. |

## Примечания

Используйте[`Reflection`](../shapebase/reflection/) свойство для доступа к свойствам отражения объекта. Вы не создаете экземпляры`ReflectionFormat` класс напрямую.

## Примеры

Показывает, как взаимодействовать с эффектом формы отражения.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
