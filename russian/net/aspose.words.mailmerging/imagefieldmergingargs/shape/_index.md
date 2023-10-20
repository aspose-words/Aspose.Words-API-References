---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words для .NET
description: ImageFieldMergingArgs Shape свойство. Указывает форму которую механизм слияния почты должен вставить в документ на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Указывает форму, которую механизм слияния почты должен вставить в документ.

```csharp
public Shape Shape { get; set; }
```

## Примечания

Если указано это свойство, механизм слияния почты игнорирует все другие свойства, такие как[`ImageFileName`](../imagefilename/) или[`ImageStream`](../imagestream/) и просто вставляет фигуру в документ.

Используйте это свойство, чтобы полностью контролировать процесс объединения поля слияния изображений. Например, вы можете указать[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/) или любое другое свойство формы для точной настройки результирующего узла. Однако обратите внимание, что вы несете ответственность за предоставление содержимого фигуры.

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
