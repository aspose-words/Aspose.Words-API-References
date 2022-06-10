---
title: Document
second_title: Справочник по API Aspose.Words для .NET
description: Создает пустой документ Word.
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

Размер бумаги документа по умолчанию Letter. Если вы хотите изменить настройку страницы, используйте [`Section.PageSetup`](../../section/pagesetup) .

После создания вы можете использовать[`DocumentBuilder`](../../documentbuilder)для простого добавления содержимого документа.

### Примеры

Показывает, как форматировать фрагмент текста, используя его свойство шрифта.

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

* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой необходимо сообщить разработчикам Aspose.Words. |
| IOException | Исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentException | Имя файла не может быть нулевым или пустой строкой. |

### Примеры

Показывает, как открыть документ и преобразовать его в .PDF.

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

Показывает, как преобразовать PDF в .docx.

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

* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой необходимо сообщить разработчикам Aspose.Words. |
| IOException | Исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentException | Имя файла не может быть нулевым или пустой строкой. |

### Примеры

Показывает, как загрузить зашифрованный документ Microsoft Word.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой необходимо сообщить разработчикам Aspose.Words. |
| IOException | Исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentNullException | Поток не может быть нулевым. |
| NotSupportedException | Поток не поддерживает чтение или поиск. |
| ObjectDisposedException | Поток является удаляемым объектом. |

### Примечания

Документ должен храниться в начале потока. Поток должен поддерживать случайное позиционирование.

### Примеры

Показывает, как загрузить документ с помощью потока.

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

Показывает, как загрузить документ с URL-адреса.

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

* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Формат документа не распознан или не поддерживается. |
| [FileCorruptedException](../../filecorruptedexception) | Документ поврежден и не может быть загружен. |
| Exception | С документом возникла проблема, о которой необходимо сообщить разработчикам Aspose.Words. |
| IOException | Исключение ввода/вывода. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Документ зашифрован, и для его открытия требуется пароль, но вы указали неправильный пароль. |
| ArgumentNullException | Поток не может быть нулевым. |
| NotSupportedException | Поток не поддерживает чтение или поиск. |
| ObjectDisposedException | Поток является удаляемым объектом. |

### Примечания

Документ должен храниться в начале потока. Поток должен поддерживать случайное позиционирование.

### Примеры

Показывает, как сохранить веб-страницу в виде файла .docx.

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

Показывает, как открыть документ HTML с изображениями из потока, используя базовый URI.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
