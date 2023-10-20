---
title: Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Document строитель. Создает пустой документ Word на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/document/document/
---
## Document() {#constructor}

Создает пустой документ Word.

```csharp
public Document()
```

## Примечания

По умолчанию формат бумаги документа — Letter. Если вы хотите изменить настройку страницы, используйте [`PageSetup`](../../section/pagesetup/).

После создания вы можете использовать[`DocumentBuilder`](../../documentbuilder/) чтобы легко добавлять содержимое документа.

## Примеры

Показывает, как форматировать фрагмент текста, используя его свойство шрифта.

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
// Существует два способа создания объекта Document с использованием Aspose.Words.
// 1 - Создать пустой документ:
Document doc = new Document();

// Новые объекты документа по умолчанию имеют минимальный набор узлов
// требуется, чтобы начать добавлять контент, такой как текст и фигуры: раздел, тело и абзац.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Загрузить документ, существующий в локальной файловой системе:
doc = new Document(MyDir + "Document.docx");

// Загруженные документы будут иметь содержимое, к которому мы сможем получить доступ и редактировать.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Некоторые операции, которые необходимо выполнить во время загрузки, например, использование пароля для расшифровки документа,
// это можно сделать, передав объект LoadOptions при загрузке документа.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Document(*string*) {#constructor_3}

Открывает существующий документ из файла. Автоматически определяет формат файла.

```csharp
public Document(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла документа, который нужно открыть. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознается или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentException | Имя файла не может быть нулевым или пустой строкой. |

## Примеры

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

// Загрузите PDF-документ, который мы только что сохранили, и преобразуйте его в .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

Показывает, как загрузить PDF-файл.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Document(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_4}

Открывает существующий документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования.

```csharp
public Document(string fileName, LoadOptions loadOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла документа, который нужно открыть. |
| loadOptions | LoadOptions | Дополнительные параметры, которые можно использовать при загрузке документа. Возможно`нулевой`. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознается или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentException | Имя файла не может быть нулевым или пустой строкой. |

## Примеры

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Существует два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

Показывает, как создавать и загружать документы.

```csharp
// Существует два способа создания объекта Document с использованием Aspose.Words.
// 1 - Создать пустой документ:
Document doc = new Document();

// Новые объекты документа по умолчанию имеют минимальный набор узлов
// требуется, чтобы начать добавлять контент, такой как текст и фигуры: раздел, тело и абзац.
doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

// 2 - Загрузить документ, существующий в локальной файловой системе:
doc = new Document(MyDir + "Document.docx");

// Загруженные документы будут иметь содержимое, к которому мы сможем получить доступ и редактировать.
Assert.AreEqual("Hello World!", doc.FirstSection.Body.FirstParagraph.GetText().Trim());

// Некоторые операции, которые необходимо выполнить во время загрузки, например, использование пароля для расшифровки документа,
// это можно сделать, передав объект LoadOptions при загрузке документа.
doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));

Assert.AreEqual("Test encrypted document.", doc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Document(*Stream*) {#constructor_1}

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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознается или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentNullException | Поток не может быть нулевым. |
| NotSupportedException | Поток не поддерживает чтение или поиск. |
| ObjectDisposedException | Поток — это удаленный объект. |

## Примечания

Документ должен храниться в начале потока. Поток должен поддерживать случайное позиционирование.

## Примеры

Показывает, как загрузить документ с помощью потока.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.docx"))
{
    Document doc = new Document(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

Показывает, как загрузить документ по URL-адресу.

```csharp
// Создайте URL-адрес, указывающий на документ Microsoft Word.
const string url = "https://filesamples.com/samples/document/docx/sample3.docx";

// Загрузите документ в массив байтов, затем загрузите этот массив в документ, используя поток памяти.
using (HttpClient webClient = new HttpClient())
{
    byte[] dataBytes = await webClient.GetByteArrayAsync(url);

    using (MemoryStream byteStream = new MemoryStream(dataBytes))
    {
        Document doc = new Document(byteStream);

        // На этом этапе мы можем прочитать и отредактировать содержимое документа, а затем сохранить его в локальной файловой системе.
        Assert.AreEqual("There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. " +
            "The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " +
            "The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.",                         
            doc.FirstSection.Body.Paragraphs[3].GetText().Trim());

        doc.Save(ArtifactsDir + "Document.LoadFromWeb.docx");
    }
}
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Document(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_2}

Открывает существующий документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования.

```csharp
public Document(Stream stream, LoadOptions loadOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, из которого загрузить документ. |
| loadOptions | LoadOptions | Дополнительные параметры, которые можно использовать при загрузке документа. Возможно`нулевой`. |

### Исключения

| исключение | условие |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Формат документа не распознается или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception/) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой следует сообщить разработчикам Aspose.Words. |
| IOException | Существует исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentNullException | Поток не может быть нулевым. |
| NotSupportedException | Поток не поддерживает чтение или поиск. |
| ObjectDisposedException | Поток — это удаленный объект. |

## Примечания

Документ должен храниться в начале потока. Поток должен поддерживать случайное позиционирование.

## Примеры

Показывает, как открыть документ HTML с изображениями из потока, используя базовый URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Передаем URI базовой папки при ее загрузке
    // чтобы можно было найти любые изображения с относительными URI в документе HTML.
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

Показывает, как загрузить зашифрованный документ Microsoft Word.

```csharp
Document doc;

// Aspose.Words выдает исключение, если мы пытаемся открыть зашифрованный документ без пароля.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// При загрузке такого документа пароль передается конструктору документа с помощью объекта LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Существует два способа загрузки зашифрованного документа с помощью объекта LoadOptions.
// 1 - Загрузить документ из локальной файловой системы по имени файла:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Загрузить документ из потока:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
