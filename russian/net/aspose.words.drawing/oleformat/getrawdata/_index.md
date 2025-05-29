---
title: OleFormat.GetRawData
linktitle: GetRawData
articleTitle: GetRawData
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetRawData в OleFormat, позволяющий легко извлекать необработанные данные объектов OLE, расширяя возможности управления данными и их интеграции.
type: docs
weight: 150
url: /ru/net/aspose.words.drawing/oleformat/getrawdata/
---
## OleFormat.GetRawData method

Получает необработанные данные объекта OLE.

```csharp
public byte[] GetRawData()
```

## Примеры

Показывает, как получить доступ к необработанным данным встроенного OLE-объекта.

```csharp
Document doc = new Document(MyDir + "OLE objects.docx");

foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true))
{
    OleFormat oleFormat = shape.OleFormat;
    if (oleFormat != null)
    {
        Console.WriteLine($"This is {(oleFormat.IsLink ? "a linked" : "an embedded")} object");
        byte[] oleRawData = oleFormat.GetRawData();

        Assert.AreEqual(24576, oleRawData.Length);
    }
}
```

### Смотрите также

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
