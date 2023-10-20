---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: Aspose.Words для .NET
description: OleFormat SuggestedFileName свойство. Получает имя файла предложенное для текущего внедренного объекта если вы хотите сохранить его в файл на С#.
type: docs
weight: 130
url: /ru/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Получает имя файла, предложенное для текущего внедренного объекта, если вы хотите сохранить его в файл.

```csharp
public string SuggestedFileName { get; }
```

## Примеры

Показывает, как получить предложенное имя файла объекта OLE.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// Объекты OLE могут предоставлять предлагаемое имя и расширение файла,
// который мы можем использовать при сохранении содержимого объекта в файл в локальной файловой системе.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Смотрите также

* class [OleFormat](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
