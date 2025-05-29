---
title: Document.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words для .NET
description: Получите оригинальное имя файла вашего документа без усилий с помощью свойства Document OriginalFileName. Улучшите свой рабочий процесс и организацию сегодня!
type: docs
weight: 300
url: /ru/net/aspose.words/document/originalfilename/
---
## Document.OriginalFileName property

Получает исходное имя файла документа.

```csharp
public string OriginalFileName { get; }
```

## Примечания

Возвраты`нулевой` если документ был загружен из потока или создан пустым.

## Примеры

Показывает, как получить сведения об операции загрузки документа.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```csharp
// Загрузить документ из файла, у которого отсутствует расширение, а затем определить формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Ниже приведены два метода преобразования LoadFormat в соответствующий ему SaveFormat.
    // 1 - Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Преобразовать LoadFormat непосредственно в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Загружаем документ из потока, а затем сохраняем его в автоматически обнаруженном расширении файла.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
