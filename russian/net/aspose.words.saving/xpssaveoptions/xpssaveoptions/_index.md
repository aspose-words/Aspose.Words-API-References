---
title: XpsSaveOptions.XpsSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: XpsSaveOptions строитель. Инициализирует новый экземпляр этого класса который можно использовать для сохранения документа document вXps формат.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа document вXps формат.

```csharp
public XpsSaveOptions()
```

### Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного документа XPS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки, которые могут служить записями оглавления уровней 1, 2, а затем 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Создаем объект «XpsSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в документ .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Выходной документ XPS будет содержать структуру, оглавление, в котором перечислены заголовки в теле документа.
// Нажатие на запись в этом контуре приведет нас к местоположению соответствующего заголовка.
// Установите для свойства «HeadingsOutlineLevels» значение «2», чтобы исключить из структуры все заголовки, уровни которых выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Смотрите также

* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../xpssaveoptions/)
* сборка [Aspose.Words](../../../)

---

## XpsSaveOptions(SaveFormat) {#constructor_1}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа document вXps илиOpenXps формат.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

### Примеры

Показывает, как сохранить документ в формате XPS в виде сгиба книги.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Создаем объект «XpsSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в документ .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Установите для свойства UseBookFoldPrintingSettings значение «true», чтобы упорядочить содержимое
// в выходном файле XPS таким образом, чтобы его можно было использовать для создания буклета.
// Установите для свойства UseBookFoldPrintingSettings значение «false», чтобы нормально отображать XPS.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Если мы отображаем документ как буклет, мы должны установить «MultiplePages»
// свойства объектов настройки страницы всех разделов равны "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Распечатав этот документ, мы можем превратить его в буклет, сложив страницы стопкой
// выйти из принтера и сложить посередине.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../xpssaveoptions/)
* сборка [Aspose.Words](../../../)


