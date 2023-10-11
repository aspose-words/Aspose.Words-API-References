---
title: FileFormatUtil.SaveFormatToLoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatUtil метод. ПреобразуетSaveFormat ценность дляLoadFormat значение если возможно.
type: docs
weight: 90
url: /ru/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Преобразует[`SaveFormat`](../../saveformat/) ценность для[`LoadFormat`](../../loadformat/) значение, если возможно.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Выдает, когда невозможно преобразовать. |

### Примеры

Показывает, как преобразовать формат сохранения в соответствующий формат загрузки.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Некоторые типы файлов могут содержать документы, сохраненные, но не загруженные с помощью Aspose.Words.
// Если мы попытаемся преобразовать формат сохранения такого типа в формат загрузки, будет выдано исключение.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Смотрите также

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../fileformatutil/)
* сборка [Aspose.Words](../../../)


