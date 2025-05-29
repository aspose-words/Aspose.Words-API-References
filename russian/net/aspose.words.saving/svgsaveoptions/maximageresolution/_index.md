---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words для .NET
description: Управляйте качеством экспортируемых растровых изображений с помощью SvgSaveOptions MaxImageResolution. Установите плотность пикселей для оптимальных результатов. По умолчанию 0.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Возвращает или задает значение в пикселях на дюйм, которое ограничивает разрешение экспортируемых растровых изображений. Значение по умолчанию — ноль.

```csharp
public int MaxImageResolution { get; set; }
```

## Примечания

Если значение этого свойства не равно нулю, оно ограничивает разрешение экспортируемых растровых изображений. То есть изображения с более высоким разрешением повторно снимаются до предела, а изображения с более низким разрешением экспортируются как есть.

Если значение этого свойства равно нулю, все растровые изображения экспортируются без передискретизации.

## Примеры

Показывает, как установить ограничение на разрешение изображения.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Смотрите также

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
