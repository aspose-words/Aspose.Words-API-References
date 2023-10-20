---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words для .NET
description: PdfSaveOptions OutlineOptions свойство. Позволяет указать параметры контура на С#.
type: docs
weight: 240
url: /ru/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Позволяет указать параметры контура.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Примечания

Контуры можно создавать из заголовков и закладок.

Для заголовков уровень структуры определяется уровнем заголовка.

Можно установить максимальный уровень заголовка для включения в контуры или вообще отключить контуры заголовков.

Уровень структуры закладок можно установить в настройках как значение по умолчанию для всех закладок или как отдельные значения для отдельных закладок.

Кроме того, контуры можно экспортировать в формат XPS, используя тот же`OutlineOptions` сорт.

## Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного PDF-документа.

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

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление со списком заголовков в теле документа.
// Нажатие на запись в этом контуре приведет нас к местоположению соответствующего заголовка.
// Установите для свойства «HeadingsOutlineLevels» значение «2», чтобы исключить из структуры все заголовки, уровни которых выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Показывает, как работать с уровнями структуры, не содержащими соответствующих заголовков, при сохранении документа PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем заголовки, которые могут служить записями оглавления уровней 1 и 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление со списком заголовков в теле документа.
// Нажатие на запись в этом контуре приведет нас к местоположению соответствующего заголовка.
// Установите для свойства «HeadingsOutlineLevels» значение «5», чтобы включить в структуру все заголовки уровней 5 и ниже.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Этот документ содержит заголовки уровней 1 и 5 и не содержит заголовков уровней 2, 3 и 4.
// Выходной PDF-документ будет считать уровни структуры 2, 3 и 4 «отсутствующими».
// Установите для свойства CreateMissingOutlineLevels значение «true», чтобы включить в структуру все недостающие уровни,
// оставляем пустые записи структуры, поскольку нет пригодных для использования заголовков.
// Установите для свойства «CreateMissingOutlineLevels» значение «false», чтобы игнорировать отсутствующие уровни структуры,
// и рассматривать заголовки уровня структуры 5 как уровень 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Смотрите также

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
