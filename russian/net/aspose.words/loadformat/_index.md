---
title: LoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: Указывает формат загружаемого документа.
type: docs
weight: 3300
url: /ru/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Указывает формат загружаемого документа.

```csharp
public enum LoadFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Инструктирует Aspose.Words автоматически распознавать формат. |
| Doc | `10` | Microsoft Word 95 или Word 97 - Документ 2003 года. |
| Dot | `11` | Шаблон Microsoft Word 95 или Word 97 - 2003. |
| DocPreWord60 | `12` | Документ имеет формат до Word 95. В настоящее время Aspose.Words не поддерживает загрузку таких документов. |
| Docx | `20` | Документ Office Open XML WordprocessingML (без макросов). |
| Docm | `21` | Документ Office Open XML WordprocessingML с поддержкой макросов. |
| Dotx | `22` | Шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | `23` | Шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| FlatOpc | `24` | Office Open XML WordprocessingML хранится в плоском XML-файле, а не в ZIP-архиве. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Macro-Enabled Документ, хранящийся в плоском файле XML вместо ZIP-пакета. |
| FlatOpcTemplate | `26` | Шаблон Office Open XML WordprocessingML (без макросов), хранящийся в плоском файле XML вместо ZIP-пакета. |
| FlatOpcTemplateMacroEnabled | `27` | Шаблон Office Open XML WordprocessingML с поддержкой макросов, хранящийся в плоском файле XML вместо ZIP-пакета. |
| Rtf | `30` | Формат RTF. |
| WordML | `31` | Формат Microsoft Word 2003 WordprocessingML. |
| Html | `50` | Формат HTML. |
| Mhtml | `51` | Формат MHTML (веб-архив). |
| Mobi | `52` | Формат MOBI. Используется считывателями MobiPocket и Amazon Kindle. |
| Chm | `53` | Формат CHM (скомпилированная HTML-справка). |
| Azw3 | `54` | Формат AZW3. Используется читателями Amazon Kindle. |
| Epub | `55` | Формат EPUB. |
| Odt | `60` | Текстовый документ ODF. |
| Ott | `61` | Шаблон текстового документа ODF. |
| Text | `62` | Обычный текст. |
| Markdown | `63` | Текстовый документ Markdown. |
| Pdf | `64` | PDF-документ. |
| Xml | `65` | XML-документ. |
| Unknown | `255` | Нераспознанный формат, не может быть загружен Aspose.Words. |

### Примеры

Показывает, как сохранить веб-страницу в виде файла .docx.

```csharp
 // Загрузить документ из файла, в котором отсутствует расширение файла, а затем определить его формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

     // Ниже приведены два метода преобразования LoadFormat в соответствующий ему SaveFormat.
     // 1 - Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки: 
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

     // 2 - Конвертировать LoadFormat напрямую в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

     // Загружаем документ из потока, а затем сохраняем его в файл с автоматически обнаруженным расширением.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

Показывает, как указать базовый URI при открытии html-документа.

```csharp
 // Загрузить документ из файла, в котором отсутствует расширение файла, а затем определить его формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

     // Ниже приведены два метода преобразования LoadFormat в соответствующий ему SaveFormat.
     // 1 - Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки: 
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

     // 2 - Конвертировать LoadFormat напрямую в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

     // Загружаем документ из потока, а затем сохраняем его в файл с автоматически обнаруженным расширением.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```csharp
 // Загрузить документ из файла, в котором отсутствует расширение файла, а затем определить его формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

     // Ниже приведены два метода преобразования LoadFormat в соответствующий ему SaveFormat.
     // 1 - Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки: 
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

     // 2 - Конвертировать LoadFormat напрямую в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

     // Загружаем документ из потока, а затем сохраняем его в файл с автоматически обнаруженным расширением.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
