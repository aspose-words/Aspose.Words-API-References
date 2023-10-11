---
title: Enum ImlRenderingMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ImlRenderingMode перечисление. Указывает как объекты рукописного ввода InkML преобразуются в фиксированные форматы страниц.
type: docs
weight: 5250
url: /ru/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Указывает, как объекты рукописного ввода (InkML) преобразуются в фиксированные форматы страниц.

```csharp
public enum ImlRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Fallback | `0` | Если для объекта рукописного ввода (InkML) доступна резервная форма, Aspose.Words отображает резервную форму вместо InkML. |
| InkML | `1` | Aspose.Words игнорирует резервную форму объекта рукописного ввода (InkML) и отображает сам InkML. Это режим по умолчанию. |

### Примеры

Показывает, как визуализировать объект Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Установка 'ImlRenderingMode.InkML' игнорирует резервную форму объекта рукописного ввода (InkML) и отображает сам InkML.
// Если результат рендеринга неудовлетворительный,
// используйте ImlRenderingMode.Fallback, чтобы получить результат, аналогичный предыдущим версиям.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


