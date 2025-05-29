---
title: Document.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: С легкостью сохраняйте документы с помощью нашего интеллектуального метода сохранения, который автоматически выбирает нужный формат на основе расширения файла для бесперебойного хранения.
type: docs
weight: 750
url: /ru/net/aspose.words/document/save/
---
## Save(*string*) {#save_2}

Сохраняет документ в файл. Автоматически определяет формат сохранения по расширению.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя документа. Если документ с указанным именем файла the уже существует, существующий документ перезаписывается. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

## Примеры

Показывает, как открыть документ и преобразовать его в формат .PDF.

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

// Загружаем PDF-документ, который мы только что сохранили, и конвертируем его в .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.pdf");

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocx.docx");
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Save(*string, [SaveFormat](../../saveformat/)*) {#save_3}

Сохраняет документ в файл в указанном формате.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя документа. Если документ с указанным именем файла the уже существует, существующий документ перезаписывается. |
| saveFormat | SaveFormat | Формат, в котором следует сохранить документ. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

## Примеры

Показывает, как конвертировать формат DOCX в HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Save(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_4}

Сохраняет документ в файл, используя указанные параметры сохранения.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя документа. Если документ с указанным именем файла the уже существует, существующий документ перезаписывается. |
| saveOptions | SaveOptions | Указывает параметры, которые управляют сохранением документа. Может быть`нулевой`. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

## Примеры

Показывает, как улучшить качество визуализированного документа с помощью SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

Показывает, как преобразовать PDF-файл в .docx и настроить процесс сохранения с помощью объекта SaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Загружаем PDF-документ, который мы только что сохранили, и конвертируем его в .docx.
Document pdfDoc = new Document(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);

// Установите свойство «Пароль», чтобы зашифровать сохраненный документ паролем.
saveOptions.Password = "MyPassword";

pdfDoc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.docx", saveOptions);
```

Показывает, как преобразовать каждую страницу документа в отдельное изображение TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Установите свойство "PageSet" на номер первой страницы из
    // с которого начать рендеринг документа.
    options.PageSet = new PageSet(i);
    // Экспортировать страницу с разрешением 2325x5325 пикселей и 600 точек на дюйм.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Показывает, как преобразовать одну страницу документа в изображение JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Установите "PageSet" на "1", чтобы выбрать вторую страницу через
// индекс (начиная с нуля), с которого начинается рендеринг документа.
options.PageSet = new PageSet(1);

// Когда мы сохраняем документ в формате JPEG, Aspose.Words отображает только одну страницу.
// Это изображение будет содержать одну страницу, начиная со второй страницы,
// которая будет просто второй страницей исходного документа.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Показывает, как настроить сжатие при сохранении документа в формате JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Установите свойство «JpegQuality» на «10», чтобы использовать более сильное сжатие при рендеринге документа.
// Это уменьшит размер файла документа, но на изображении будут видны более заметные артефакты сжатия.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Установите свойство «JpegQuality» на «100», чтобы использовать более слабое сжатие при визуализации документа.
// Это улучшит качество изображения за счет увеличения размера файла.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Показывает, как преобразовать весь документ в PDF с тремя уровнями в структуре документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки уровней с 1 по 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "4", чтобы исключить из структуры все заголовки, уровни которых выше 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Если запись структуры имеет последующие записи более высокого уровня между собой и следующей записью того же или более низкого уровня,
// слева от записи появится стрелка. Эта запись является «владельцем» нескольких таких «подзаписей».
// В нашем документе записи структуры из 5-го уровня заголовка являются подзаписями второй записи структуры 4-го уровня,
// записи 4-го и 5-го уровня заголовка являются подзаголовками второй записи 3-го уровня и т. д.
// В схеме мы можем щелкнуть стрелку записи «владелец», чтобы свернуть/развернуть все ее подзаписи.
// Установите свойство "ExpandedOutlineLevels" на "2", чтобы автоматически развернуть все заголовки уровня 2 и более низких записей структуры
// и сворачиваем все записи уровня 3 и выше при открытии документа.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Save(*Stream, [SaveFormat](../../saveformat/)*) {#save}

Сохраняет документ в потоке, используя указанный формат.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Укажите, где сохранить документ. |
| saveFormat | SaveFormat | Формат, в котором следует сохранить документ. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

## Примеры

Показывает, как сохранить документ в потоке.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Проверяем, что поток содержит документ.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Показывает, как сохранить документ в виде изображения через поток, а затем прочитать изображение из этого потока.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET461_OR_GREATER || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Считываем поток обратно в изображение.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                SKCodec codec = SKCodec.Create(stream);
                Assert.AreEqual(SKEncodedImageFormat.Bmp, codec.EncodedFormat);

                stream.Position = 0;

                using (SKBitmap image = SKBitmap.Decode(stream))
                {
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#endif
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Save(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_1}

Сохраняет документ в потоке, используя указанные параметры сохранения.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Укажите, где сохранить документ. |
| saveOptions | SaveOptions | Указывает параметры, которые управляют сохранением документа. Может быть`нулевой` . Если это`нулевой`, документ будет сохранен в двоичном формате DOC. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

## Примеры

Показывает, как преобразовать в PDF только некоторые страницы документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ преобразования этим методом документа в .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Установите «PageIndex» на «1», чтобы отобразить часть документа, начиная со второй страницы.
    options.PageSet = new PageSet(1);

    // Этот документ будет содержать одну страницу, начиная со страницы два, которая будет содержать только вторую страницу.
    doc.Save(stream, options);
}
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Save(*HttpResponse, string, [ContentDisposition](../../contentdisposition/), [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#save_5}

Отправляет документ в клиентский браузер.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| response | HttpResponse | Объект ответа, где сохранить документ. |
| fileName | String | Имя документа, которое будет отображаться в клиентском браузере. Имя не должно содержать путь. |
| contentDisposition | ContentDisposition | А[`ContentDisposition`](../../contentdisposition/) значение that определяет, как документ отображается в клиентском браузере. |
| saveOptions | SaveOptions | Указывает параметры, которые управляют сохранением документа. Может быть`нулевой`. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

## Примечания

Внутренне этот метод сначала сохраняет данные в потоке памяти, а затем копирует их в поток ответа stream , поскольку поток ответа не поддерживает поиск.

## Примеры

Показывает, как выполнить слияние почты, а затем сохранить документ в клиентском браузере.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Отправляем документ в клиентский браузер.
//Выброшено, потому что HttpResponse имеет значение null в тесте.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим в документ лишнего содержимого после сохранения.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
