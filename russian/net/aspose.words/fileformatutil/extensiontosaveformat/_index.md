---
title: FileFormatUtil.ExtensionToSaveFormat
linktitle: ExtensionToSaveFormat
articleTitle: ExtensionToSaveFormat
second_title: Aspose.Words для .NET
description: Легко преобразуйте расширения имен файлов в значения SaveFormat с помощью метода FileFormatUtil ExtensionToSaveFormat. Упростите управление файлами уже сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Преобразует расширение имени файла в[`SaveFormat`](../../saveformat/) значение.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| extension | String | Расширение файла. Может быть с точкой в начале или без нее. Нечувствительно к регистру. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, если параметр равен`нулевой`. |

## Примечания

Если расширение не может быть распознано, возвращаетUnknown.

## Примеры

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

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
