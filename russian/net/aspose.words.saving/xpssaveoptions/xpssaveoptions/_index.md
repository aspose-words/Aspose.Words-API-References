---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор XpsSaveOptions, который позволит легко создавать экземпляры для сохранения документов в формате XPS, повышая эффективность управления документами.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вXps формат.

```csharp
public XpsSaveOptions()
```

## Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного документа XPS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки, которые могут служить записями оглавления уровней 1, 2 и 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Создаем объект "XpsSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Выходной документ XPS будет содержать структуру, оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "2", чтобы исключить из структуры все заголовки, уровни которых выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Смотрите также

* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вXps илиOpenXps формат.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## Примеры

Показывает, как сохранить документ в формате XPS в виде книжного сгиба.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект "XpsSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Установите свойство "UseBookFoldPrintingSettings" в значение "true", чтобы упорядочить содержимое
// в выходном XPS-файле таким образом, чтобы его можно было использовать для создания буклета.
// Установите свойство «UseBookFoldPrintingSettings» в значение «false» для обычной визуализации XPS.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Если мы визуализируем документ как брошюру, мы должны установить "MultiplePages"
// свойства объектов настройки страницы всех разделов на "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// После того, как мы распечатаем этот документ, мы можем превратить его в брошюру, сложив страницы
// чтобы вынуть из принтера и сложить пополам.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
