---
title: Document.Document
second_title: Справочник по API Aspose.Words для .NET
description: Document строитель. Создает пустой документ Word.
type: docs
weight: 10
url: /ru/net/aspose.words/document/document/
---
## Document() {#constructor}

Создает пустой документ Word.

```csharp
public Document()
```

### Примечания

Размер бумаги документа по умолчанию — Letter. Если вы хотите изменить настройки страницы, используйте [`Раздел.PageSetup`](../../section/pagesetup/).

После создания вы можете использовать[`DocumentBuilder`](../../documentbuilder/) легко добавлять содержимое документа.

### Примеры

Показывает, как отформатировать набор текста, используя его свойство шрифта.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Показывает, как создавать и загружать документы.

```csharp
// Существует два способа создания объекта Document с помощью Aspose.Words.
// 1 - Создать пустой документ:
Document doc = new Document();

// Новые объекты Document по умолчанию имеют минимальный набор узлов
// требуется для начала добавления содержимого, такого как текст и фигуры: раздел, основной текст и абзац.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Загрузить документ, существующий в локальной файловой системе:
doc = new Document(MyDir + "Document.docx");

// Загруженные документы будут иметь содержимое, к которому мы можем получить доступ и редактировать.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Некоторые операции, которые должны выполняться во время загрузки, например, использование пароля для расшифровки документа,
// можно сделать, передав объект LoadOptions при загрузке документа.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Document(string) {#constructor_3}

Открывает существующий документ из файла. Автоматически определяет формат файла.

```csharp
public Document(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла открываемого документа. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | Возникла проблема с документом, о ней следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неверный пароль. |
| ArgumentException | Имя файла не может быть нулевым или пустой строкой. |

### Примеры

Показывает, как открыть документ и преобразовать его в .PDF.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToPdf.pdf");
```

Показывает, как преобразовать PDF в .docx.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

// Загрузите документ PDF, который мы только что сохранили, и преобразуйте его в .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Показывает, как загрузить PDF.

```csharp
Aspose.Words.Document doc = new Aspose.Words.Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

// Ниже приведены два способа загрузки PDF-документов с помощью продуктов Aspose.
// 1 - Загрузить как документ Aspose.Words:
Aspose.Words.Document asposeWordsDoc = new Aspose.Words.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

Assert.AreEqual("Hello world!", asposeWordsDoc.GetText().Trim());

// 2 - Загрузить как документ Aspose.Pdf:
Aspose.Pdf.Document asposePdfDoc = new Aspose.Pdf.Document(ArtifactsDir + "PDF2Word.LoadPdf.pdf");

TextFragmentAbsorber textFragmentAbsorber = new TextFragmentAbsorber();
asposePdfDoc.Pages.Accept(textFragmentAbsorber);

Assert.AreEqual("Hello world!", textFragmentAbsorber.Text.Trim());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Document(string, LoadOptions) {#constructor_4}

Открывает существующий документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла открываемого документа. |
| loadOptions | LoadOptions | Дополнительные параметры для использования при загрузке документа. Может быть нулевым. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | Возникла проблема с документом, о ней следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неверный пароль. |
| ArgumentException | Имя файла не может быть нулевым или пустой строкой. |

### Примеры

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Есть два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

Показывает, как создавать и загружать документы.

```csharp
// Существует два способа создания объекта Document с помощью Aspose.Words.
// 1 - Создать пустой документ:
Document doc = new Document();

// Новые объекты Document по умолчанию имеют минимальный набор узлов
// требуется для начала добавления содержимого, такого как текст и фигуры: раздел, основной текст и абзац.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Загрузить документ, существующий в локальной файловой системе:
doc = new Document(MyDir + "Document.docx");

// Загруженные документы будут иметь содержимое, к которому мы можем получить доступ и редактировать.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Некоторые операции, которые должны выполняться во время загрузки, например, использование пароля для расшифровки документа,
// можно сделать, передав объект LoadOptions при загрузке документа.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Document(Stream) {#constructor_1}

Открывает существующий документ из потока. Автоматически определяет формат файла.

```csharp
public Document(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, откуда загрузить документ. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | Возникла проблема с документом, о ней следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неверный пароль. |
| ArgumentNullException | Поток не может быть нулевым. |
| NotSupportedException | Поток не поддерживает чтение или поиск. |
| ObjectDisposedException | Поток — это удаленный объект. |

### Примечания

Документ должен храниться в начале потока. Поток должен поддерживать случайное позиционирование.

### Примеры

Показывает, как загрузить документ с помощью потока.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Показывает, как загрузить документ из URL-адреса.

```csharp
// Создайте URL-адрес, указывающий на документ Microsoft Word.
const string url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx";

// Загрузите документ в массив байтов, затем загрузите этот массив в документ, используя поток памяти.
using (WebClient webClient = new WebClient())
{
    byte[] dataBytes = webClient.DownloadData(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // На этом этапе мы можем прочитать и отредактировать содержимое документа, а затем сохранить его в локальной файловой системе.
        Assert.AreEqual("Use this section to highlight your relevant passions, activities, and how you like to give back. " +
                        "It’s good to include Leadership and volunteer experiences here. " +
                        "Or show off important extras like publications, certifications, languages and more.",
            doc.FirstSection.Body.Paragraphs[4].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Document(Stream, LoadOptions) {#constructor_2}

Открывает существующий документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, из которого загружается документ. |
| loadOptions | LoadOptions | Дополнительные параметры для использования при загрузке документа. Может быть нулевым. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | Возникла проблема с документом, о ней следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неверный пароль. |
| ArgumentNullException | Поток не может быть нулевым. |
| NotSupportedException | Поток не поддерживает чтение или поиск. |
| ObjectDisposedException | Поток — это удаленный объект. |

### Примечания

Документ должен храниться в начале потока. Поток должен поддерживать случайное позиционирование.

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

Показывает, как открыть HTML-документ с изображениями из потока, используя базовый URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Передаем URI базовой папки при ее загрузке
    // чтобы можно было найти любые изображения с относительными URI в HTML-документе.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Убедитесь, что первая фигура документа содержит допустимое изображение.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Есть два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


