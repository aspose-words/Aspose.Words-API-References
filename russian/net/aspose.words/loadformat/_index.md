---
title: LoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: Указывает формат загружаемого документа.
type: docs
weight: 3350
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
| Auto | `0` | Указывает Aspose.Words автоматически распознавать формат. |
| Doc | `10` | Microsoft Word 95 или Word 97 — документ 2003 г. |
| Dot | `11` | Microsoft Word 95 или Word 97 — шаблон 2003 года. |
| DocPreWord60 | `12` | Документ находится в формате, предшествующем Word 95. В настоящее время Aspose.Words не поддерживает загрузку таких документов. |
| Docx | `20` | Документ Office Open XML WordprocessingML (без макросов). |
| Docm | `21` | Документ Office Open XML WordprocessingML с поддержкой макросов. |
| Dotx | `22` | Шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | `23` | Шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| FlatOpc | `24` | Office Open XML WordprocessingML хранится в простом XML-файле, а не в ZIP-архиве. |
| FlatOpcMacroEnabled | `25` | Документ Office Open XML WordprocessingML с поддержкой макросов хранится в плоском XML-файле, а не в ZIP-архиве. |
| FlatOpcTemplate | `26` | Шаблон Office Open XML WordprocessingML (без макросов), хранящийся в плоском XML-файле, а не в ZIP-архиве. |
| FlatOpcTemplateMacroEnabled | `27` | Шаблон Office Open XML WordprocessingML с поддержкой макросов, хранящийся в простом XML-файле, а не в ZIP-архиве. |
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
| Text | `62` | Простой текст. |
| Markdown | `63` | Текстовый документ Markdown. |
| Pdf | `64` | PDF-документ. |
| Xml | `65` | XML-документ. |
| Unknown | `255` | Нераспознанный формат, не может быть загружен Aspose.Words. |

### Примеры

Показывает, как сохранить веб-страницу в виде файла .docx.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // URL-адрес снова используется как baseUri, чтобы убедиться, что любые относительные пути к изображениям извлекаются правильно.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Загружаем HTML-документ из потока и передаем объект LoadOptions.
        Document doc = new Document(stream, options);

        // На этом этапе мы можем прочитать и отредактировать содержимое документа, а затем сохранить его в локальной файловой системе.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Показывает, как указать базовый URI при открытии html-документа.

```csharp
// Предположим, мы хотим загрузить документ .html, содержащий изображение, связанное относительным URI
// пока изображение находится в другом месте. В этом случае нам нужно будет преобразовать относительный URI в абсолютный.
 // Мы можем предоставить базовый URI, используя объект HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Хотя изображение во входном .html было повреждено, наш собственный базовый URI помог нам восстановить ссылку.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Этот выходной документ будет отображать отсутствующее изображение.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
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
    // 1 — Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Преобразование LoadFormat напрямую в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Загрузите документ из потока, а затем сохраните его в файле с автоматически обнаруженным расширением.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
