---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words для .NET
description: PlainTextDocument строитель. Создает простой текстовый документ из файла. Автоматически определяет формат файла на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

Создает простой текстовый документ из файла. Автоматически определяет формат файла.

```csharp
public PlainTextDocument(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла, из которого нужно извлечь текст. |

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

Показывает, как загрузить содержимое документа Microsoft Word в виде открытого текста.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Смотрите также

* class [PlainTextDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Создает простой текстовый документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла, из которого нужно извлечь текст. |
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

Показывает, как загрузить содержимое зашифрованного документа Microsoft Word в виде открытого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

Создает простой текстовый документ из потока. Автоматически определяет формат файла.

```csharp
public PlainTextDocument(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, из которого извлекается текст. |

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

Показывает, как загрузить содержимое документа Microsoft Word в виде открытого текста с помощью потока.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Смотрите также

* class [PlainTextDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

Создает простой текстовый документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, из которого извлекается текст. |
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

Показывает, как загрузить содержимое зашифрованного документа Microsoft Word в виде открытого текста с помощью потока.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Смотрите также

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
