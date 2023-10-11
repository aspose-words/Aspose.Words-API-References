---
title: OutlineOptions.CreateMissingOutlineLevels
second_title: Справочник по API Aspose.Words для .NET
description: OutlineOptions свойство. Получает или задает значение определяющее создавать ли отсутствующие уровни структуры при экспорте документа .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Получает или задает значение, определяющее, создавать ли отсутствующие уровни структуры при экспорте документа .

Значение по умолчанию для этого свойства:`ЛОЖЬ`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

### Примеры

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

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../outlineoptions/)
* сборка [Aspose.Words](../../../)


