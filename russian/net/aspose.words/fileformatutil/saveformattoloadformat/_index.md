---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words для .NET
description: Легко конвертируйте SaveFormat в LoadFormat с помощью метода FileFormatUtil. Упростите управление файлами и улучшите совместимость уже сегодня!
type: docs
weight: 90
url: /ru/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Преобразует[`SaveFormat`](../../saveformat/) значение для[`LoadFormat`](../../loadformat/) значение, если возможно.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Выдает, когда не может конвертировать. |

## Примеры

Показывает, как преобразовать формат сохранения в соответствующий ему формат загрузки.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// В некоторых типах файлов можно сохранять документы, но нельзя загружать их с помощью Aspose.Words.
// Если мы попытаемся преобразовать формат сохранения такого типа в формат загрузки, будет выдано исключение.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Смотрите также

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
