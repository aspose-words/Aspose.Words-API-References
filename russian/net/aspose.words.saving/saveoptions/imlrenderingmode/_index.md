---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SaveOptions ImlRenderingMode улучшает рендеринг объектов InkML. Оптимизируйте рендеринг чернил для лучших визуальных результатов!
type: docs
weight: 90
url: /ru/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Возвращает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML).

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Примечания

Значение по умолчанию:InkML .

Это свойство используется при экспорте документа в форматы с фиксированным размером страницы.

## Примеры

Показывает, как визуализировать объект Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Установка 'ImlRenderingMode.InkML' игнорирует резервную форму объекта чернил (InkML) и отображает сам InkML.
// Если результат рендеринга неудовлетворительный,
// пожалуйста, используйте 'ImlRenderingMode.Fallback', чтобы получить результат, аналогичный предыдущим версиям.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Смотрите также

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
