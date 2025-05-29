---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.LoadFormat, определяющее форматы документов для бесперебойной загрузки и улучшенной совместимости в ваших приложениях.
type: docs
weight: 4000
url: /ru/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Указывает формат документа, который должен быть загружен.

```csharp
public enum LoadFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Указывает Aspose.Words автоматически распознавать формат. |
| MsWorks | `8` | Документ Microsoft Works 8. |
| Doc | `10` | Microsoft Word 95 или Word 97 - 2003 Документ. |
| Dot | `11` | Шаблон Microsoft Word 95 или Word 97 - 2003. |
| DocPreWord60 | `12` | Документ имеет формат, предшествующий Word 95. Aspose.Words в настоящее время не поддерживает загрузку таких документов. |
| Docx | `20` | Документ Office Open XML WordprocessingML (без макросов). |
| Docm | `21` | Документ Office Open XML WordprocessingML с поддержкой макросов. |
| Dotx | `22` | Шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | `23` | Шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| FlatOpc | `24` | Office Open XML WordprocessingML хранится в плоском XML-файле вместо ZIP-пакета. |
| FlatOpcMacroEnabled | `25` | Документ Office Open XML WordprocessingML с поддержкой макросов, сохраненный в виде простого XML-файла вместо ZIP-архива. |
| FlatOpcTemplate | `26` | Шаблон Office Open XML WordprocessingML (без макросов), сохраненный в виде простого XML-файла вместо ZIP-архива. |
| FlatOpcTemplateMacroEnabled | `27` | Шаблон Office Open XML WordprocessingML с поддержкой макросов, сохраненный в виде простого XML-файла вместо ZIP-архива. |
| Rtf | `30` | Формат RTF. |
| WordML | `31` | Формат Microsoft Word 2003 WordprocessingML. |
| Html | `50` | Формат HTML. |
| Mhtml | `51` | Формат MHTML (веб-архив). |
| Mobi | `52` | Формат MOBI . Используется ридерами MobiPocket и Amazon Kindle. |
| Chm | `53` | Формат CHM (скомпилированная HTML-справка). |
| Azw3 | `54` | Формат AZW3. Используется в читалках Amazon Kindle. |
| Epub | `55` | Формат EPUB. |
| Odt | `60` | Текстовый документ ODF. |
| Ott | `61` | Шаблон текстового документа ODF. |
| Text | `62` | Обычный текст. |
| Markdown | `63` | Текстовый документ Markdown. |
| Pdf | `64` | PDF-документ. |
| Xml | `65` | XML-документ. |
| Unknown | `255` | Нераспознанный формат, не может быть загружен Aspose.Words. |

## Примеры

Показывает, как сохранить веб-страницу в виде файла .docx.

```csharp
const string url = "https://products.aspose.com/words/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL-адрес снова используется как baseUri, чтобы гарантировать правильность извлечения любых относительных путей к изображениям.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // Загружаем HTML-документ из потока и передаем объект LoadOptions.
        Document doc = new Document(stream, options);

        // На этом этапе мы можем прочитать и отредактировать содержимое документа, а затем сохранить его в локальной файловой системе.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Показывает, как указать базовый URI при открытии HTML-документа.

```csharp
// Предположим, мы хотим загрузить документ .html, содержащий изображение, связанное с помощью относительного URI
// пока изображение находится в другом месте. В этом случае нам нужно будет преобразовать относительный URI в абсолютный.
 // Мы можем предоставить базовый URI с помощью объекта HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Хотя изображение во входном .html-файле было повреждено, наш базовый URI помог нам восстановить ссылку.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Этот выходной документ будет отображать отсутствующее изображение.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
