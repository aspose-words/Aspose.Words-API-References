---
title: Enum LoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.LoadFormat перечисление. Указывает формат загружаемого документа.
type: docs
weight: 3550
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
| Doc | `10` | Документ Microsoft Word 95 или Word 97 – 2003. |
| Dot | `11` | Шаблон Microsoft Word 95 или Word 97 – 2003. |
| DocPreWord60 | `12` | Документ имеет формат, предшествующий Word 95. Aspose.Words в настоящее время не поддерживает загрузку таких документов. |
| Docx | `20` | Документ Office Open XML WordprocessingML (без макросов). |
| Docm | `21` | Документ Office Open XML WordprocessingML с поддержкой макросов. |
| Dotx | `22` | Шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | `23` | Шаблон Office Open XML WordprocessingML с поддержкой макросов. |
| FlatOpc | `24` | Office Open XML WordprocessingML хранится в простом XML-файле, а не в ZIP-пакете. |
| FlatOpcMacroEnabled | `25` | Документ Office Open XML WordprocessingML с поддержкой макросов, хранящийся в простом XML-файле, а не в ZIP-пакете. |
| FlatOpcTemplate | `26` | Шаблон Office Open XML WordprocessingML (без макросов), хранящийся в простом XML-файле, а не в ZIP-пакете. |
| FlatOpcTemplateMacroEnabled | `27` | Шаблон Office Open XML WordprocessingML с поддержкой макросов, хранящийся в простом XML-файле, а не в ZIP-пакете. |
| Rtf | `30` | Формат RTF. |
| WordML | `31` | Формат Microsoft Word 2003 WordprocessingML. |
| Html | `50` | Формат HTML. |
| Mhtml | `51` | Формат MHTML (веб-архив). |
| Mobi | `52` | Формат MOBI. Используется читателями MobiPocket и Amazon Kindle. |
| Chm | `53` | Формат CHM (скомпилированная HTML-справка). |
| Azw3 | `54` | Формат AZW3. Используется читателями Amazon Kindle. |
| Epub | `55` | Формат EPUB. |
| Odt | `60` | Текстовый документ ODF. |
| Ott | `61` | Шаблон текстового документа ODF. |
| Text | `62` | Обычный текст. |
| Markdown | `63` | Текстовый документ с уценкой. |
| Pdf | `64` | PDF-документ. |
| Xml | `65` | XML-документ. |
| Unknown | `255` | Нераспознанный формат, невозможно загрузить с помощью Aspose.Words. |

### Примеры

Показывает, как сохранить веб-страницу в виде файла .docx.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL-адрес снова используется в качестве baseUri, чтобы гарантировать правильность получения любых относительных путей к изображениям.
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
// Предположим, мы хотим загрузить документ .html, содержащий изображение, связанное относительным URI.
// пока изображение находится в другом месте. В этом случае нам нужно будет преобразовать относительный URI в абсолютный.
 // Мы можем предоставить базовый URI, используя объект HtmlLoadOptions.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Хотя изображение во входном .html было повреждено, наш собственный базовый URI помог нам восстановить ссылку.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Этот выходной документ отобразит отсутствующее изображение.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


