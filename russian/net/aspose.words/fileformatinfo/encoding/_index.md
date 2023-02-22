---
title: FileFormatInfo.Encoding
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatInfo свойство. Получает обнаруженную кодировку если она применима к текущему формату документа. На данный момент определяет кодировку только для документов HTML.
type: docs
weight: 10
url: /ru/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Получает обнаруженную кодировку, если она применима к текущему формату документа. На данный момент определяет кодировку только для документов HTML.

```csharp
public Encoding Encoding { get; }
```

### Примеры

Показывает, как определить кодировку в html-файле.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Свойство Encoding используется только при создании объекта FileFormatInfo для html-документа.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Смотрите также

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../fileformatinfo/)
* сборка [Aspose.Words](../../../)


