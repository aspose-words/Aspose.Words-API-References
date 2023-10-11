---
title: FileFormatUtil.ExtensionToSaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatUtil метод. Преобразует расширение имени файла вSaveFormat значение.
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
| extension | String | Расширение файла. Может быть с точкой в начале или без нее. Без учета регистра. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, если параметр`нулевой`. |

### Примечания

Если расширение не может быть распознано, возвращаетсяUnknown.

### Примеры

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```csharp
// Загрузите документ из файла, у которого отсутствует расширение файла, а затем определите его формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Ниже приведены два метода преобразования LoadFormat в соответствующий SaveFormat.
    // 1 — Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 — преобразовать LoadFormat непосредственно в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Загрузите документ из потока, а затем сохраните его с автоматически определенным расширением файла.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../fileformatutil/)
* сборка [Aspose.Words](../../../)


