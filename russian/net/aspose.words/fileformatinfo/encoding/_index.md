---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FileFormatInfo Encoding, чтобы без труда определить кодировку документа. В настоящее время поддерживает форматы HTML для точных результатов.
type: docs
weight: 10
url: /ru/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Получает обнаруженную кодировку, если она применима к текущему формату документа. В данный момент определяет кодировку только для документов HTML.

```csharp
public Encoding Encoding { get; }
```

## Примеры

Показывает, как определить кодировку в HTML-файле.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Свойство Encoding используется только при создании объекта FileFormatInfo для HTML-документа.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Смотрите также

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
