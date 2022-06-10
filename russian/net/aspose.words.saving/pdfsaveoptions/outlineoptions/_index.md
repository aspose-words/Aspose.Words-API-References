---
title: OutlineOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать параметры контура.
type: docs
weight: 210
url: /ru/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Позволяет указать параметры контура.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Примечания

Схемы можно создавать из заголовков и закладок.

Уровень структуры заголовков определяется уровнем заголовка.

Можно установить максимальный уровень заголовка для включения в контуры или вообще отключить контуры рубрик.

Для закладок уровень структуры может быть установлен в опциях как значение по умолчанию для всех закладок или как индивидуальное значение для отдельных закладок.

Кроме того, контуры можно экспортировать в формат XPS с помощью того же класса`OutlineOptions`.

### Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного документа PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки, которые могут служить элементами оглавления уровней 1 и 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, которая представляет собой оглавление, в котором перечислены заголовки в теле документа.
// Нажав на запись в этой схеме, мы перейдем к расположению соответствующего заголовка.
// Установите для свойства "HeadingsOutlineLevels" значение "5", чтобы включить в схему все заголовки уровня 5 и ниже.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

 // Этот документ содержит заголовки уровней 1 и 5 и не содержит заголовков уровней 2, 3 и 4.
// Выходной PDF-документ будет рассматривать уровни структуры 2, 3 и 4 как «отсутствующие».
// Установите для свойства "CreateMissingOutlineLevels" значение "true", чтобы включить в схему все отсутствующие уровни,
// оставляя пустые элементы схемы, поскольку нет подходящих заголовков.
// Установите для свойства "CreateMissingOutlineLevels" значение "false", чтобы игнорировать отсутствующие уровни структуры,
// и обрабатывать заголовки уровня 5 схемы как уровня 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

Показывает, как работать с уровнями структуры, не содержащими соответствующих заголовков, при сохранении документа PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки, которые могут служить элементами оглавления уровней 1 и 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, которая представляет собой оглавление, в котором перечислены заголовки в теле документа.
// Нажав на запись в этой схеме, мы перейдем к расположению соответствующего заголовка.
// Установите для свойства "HeadingsOutlineLevels" значение "5", чтобы включить в схему все заголовки уровня 5 и ниже.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

 // Этот документ содержит заголовки уровней 1 и 5 и не содержит заголовков уровней 2, 3 и 4.
// Выходной PDF-документ будет рассматривать уровни структуры 2, 3 и 4 как «отсутствующие».
// Установите для свойства "CreateMissingOutlineLevels" значение "true", чтобы включить в схему все отсутствующие уровни,
// оставляя пустые элементы схемы, поскольку нет подходящих заголовков.
// Установите для свойства "CreateMissingOutlineLevels" значение "false", чтобы игнорировать отсутствующие уровни структуры,
// и обрабатывать заголовки уровня 5 схемы как уровня 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Смотрите также

* class [OutlineOptions](../../outlineoptions)
* class [PdfSaveOptions](../../pdfsaveoptions)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
