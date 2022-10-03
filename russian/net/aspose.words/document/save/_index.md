---
title: Save
second_title: Справочник по API Aspose.Words для .NET
description: Сохраняет документ в файл. Автоматически определяет формат сохранения из расширения.
type: docs
weight: 680
url: /ru/net/aspose.words/document/save/
---
## Save(string) {#save_2}

Сохраняет документ в файл. Автоматически определяет формат сохранения из расширения.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя для документа. Если документ с указанным именем файла уже существует, существующий документ перезаписывается. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

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

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Save(string, SaveFormat) {#save_3}

Сохраняет документ в файл в указанном формате.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя для документа. Если документ с указанным именем файла уже существует, существующий документ перезаписывается. |
| saveFormat | SaveFormat | Формат, в котором нужно сохранить документ. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

### Примеры

Показывает, как конвертировать из формата DOCX в формат HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [SaveFormat](../../saveformat/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Save(string, SaveOptions) {#save_4}

Сохраняет документ в файл, используя указанные параметры сохранения.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя для документа. Если документ с указанным именем файла уже существует, существующий документ перезаписывается. |
| saveOptions | SaveOptions | Указывает параметры, управляющие способом сохранения документа. Может быть нулевым. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

### Примеры

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

Показывает, как преобразовать PDF в .docx и настроить процесс сохранения с помощью объекта SaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PDF2Word.ConvertPdfToDocxCustom.pdf");

// Загрузите документ PDF, который мы только что сохранили, и преобразуйте его в .docx.
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

// Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Устанавливаем в свойство "PageSet" номер первой страницы из
    // с которого начать рендеринг документа.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Показывает, как преобразовать одну страницу из документа в изображение JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// Установите для "PageSet" значение "1", чтобы выбрать вторую страницу через
// отсчитываемый от нуля индекс, с которого начинается рендеринг документа.
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

// Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Установите для свойства "JpegQuality" значение "10", чтобы использовать более сильное сжатие при рендеринге документа.
// Это уменьшит размер файла документа, но изображение будет отображать более заметные артефакты сжатия.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Установите для свойства "JpegQuality" значение "100", чтобы использовать более слабое сжатие при преобразовании документа.
// Это улучшит качество изображения за счет увеличения размера файла.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Показывает, как преобразовать весь документ в PDF с тремя уровнями структуры документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки уровней с 1 по 5.
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

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, которая представляет собой оглавление, в котором перечислены заголовки в теле документа.
// Нажав на запись в этой схеме, мы перейдем к расположению соответствующего заголовка.
// Установите для свойства "HeadingsOutlineLevels" значение "4", чтобы исключить из структуры все заголовки, уровни которых выше 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Если запись схемы имеет последующие записи более высокого уровня между собой и следующей записью того же или более низкого уровня,
// слева от записи появится стрелка. Эта запись является «владельцем» нескольких таких «подзаписей».
// В нашем документе элементы структуры с 5-го уровня заголовка являются подстатьями второго элемента структуры 4-го уровня,
 // статьи 4-го и 5-го уровня заголовков являются подстатьями второй записи 3-го уровня и т.д.
// В схеме мы можем щелкнуть стрелку записи «владелец», чтобы свернуть/развернуть все ее подзаписи.
// Установите для свойства «ExpandedOutlineLevels» значение «2», чтобы автоматически расширять все элементы уровня заголовка 2 и нижнего уровня структуры
 // и свернуть все записи уровня и 3 и выше при открытии документа.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Save(Stream, SaveFormat) {#save}

Сохраняет документ в поток, используя указанный формат.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, где сохранить документ. |
| saveFormat | SaveFormat | Формат, в котором нужно сохранить документ. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

### Примеры

Показывает, как сохранить документ в поток.

```csharp
Document doc = new Document(MyDir + "Document.docx");

using (MemoryStream dstStream = new MemoryStream())
{
    doc.Save(dstStream, SaveFormat.Docx);

    // Проверяем, что поток содержит документ.
    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", new Document(dstStream).GetText().Trim());
}
```

Показывает, как сохранить документ в изображение через поток, а затем прочитать изображение из этого потока.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

#if NET48 || JAVA
            using (MemoryStream stream = new MemoryStream())
            {
                doc.Save(stream, SaveFormat.Bmp);

                stream.Position = 0;

                // Читаем поток обратно в изображение.
                using (Image image = Image.FromStream(stream))
                {
                    Assert.AreEqual(ImageFormat.Bmp, image.RawFormat);
                    Assert.AreEqual(816, image.Width);
                    Assert.AreEqual(1056, image.Height);
                }
            }
#elif NET5_0_OR_GREATER || __MOBILE__
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
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Save(Stream, SaveOptions) {#save_1}

Сохраняет документ в поток, используя указанные параметры сохранения.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, где сохранить документ. |
| saveOptions | SaveOptions | Указывает параметры, управляющие способом сохранения документа. Может быть null. Если это значение null, документ будет сохранен в двоичном формате DOC. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

### Примеры

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
    // Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
    // для изменения того, как этот метод преобразует документ в .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Установите для "PageIndex" значение "1", чтобы отображать часть документа, начиная со второй страницы.
    options.PageSet = new PageSet(1);

    // Этот документ будет содержать одну страницу, начиная со второй страницы, которая будет содержать только вторую страницу.
    doc.Save(stream, options);
}
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Save(HttpResponse, string, ContentDisposition, SaveOptions) {#save_5}

Отправляет документ в браузер клиента.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| response | HttpResponse | Объект ответа, где сохранить документ. |
| fileName | String | Имя документа, которое появится в браузере клиента. Имя не должно содержать путь. |
| contentDisposition | ContentDisposition | А[`ContentDisposition`](../../contentdisposition/) значение that указывает, как документ представлен в клиентском браузере. |
| saveOptions | SaveOptions | Указывает параметры, управляющие способом сохранения документа. Может быть нулевым. |

### Возвращаемое значение

Дополнительная информация, которую вы можете использовать по желанию.

### Примечания

Внутри этот метод сначала сохраняет в поток памяти, а затем копирует в поток ответа , поскольку поток ответа не поддерживает поиск.

### Примеры

Показывает, как выполнить слияние почты, а затем сохранить документ в браузере клиента.

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); // Выброшено, потому что HttpResponse имеет значение null в тесте.

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим лишний контент в документ после сохранения.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Смотрите также

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* enum [ContentDisposition](../../contentdisposition/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
