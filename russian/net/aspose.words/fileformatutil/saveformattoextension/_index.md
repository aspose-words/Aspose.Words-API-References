---
title: FileFormatUtil.SaveFormatToExtension
linktitle: SaveFormatToExtension
articleTitle: SaveFormatToExtension
second_title: Aspose.Words для .NET
description: Конвертируйте значения формата сохранения в расширения файлов без усилий с помощью метода SaveFormatToExtension FileFormatUtil. Получайте точные, строчные расширения с легкостью!
type: docs
weight: 80
url: /ru/net/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil.SaveFormatToExtension method

Преобразует значение формата сохранения перечисления в расширение файла. Возвращаемое расширение — это строка в нижнем регистре с точкой в начале.

```csharp
public static string SaveFormatToExtension(SaveFormat saveFormat)
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Выдает, когда не может конвертировать. |

## Примечания

TheWordML значение преобразуется в «.wml».

TheFlatOpc значение преобразуется в «.fopc».

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
