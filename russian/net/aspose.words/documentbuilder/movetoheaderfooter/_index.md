---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words для .NET
description: Легко переходите к верхним и нижним колонтитулам с помощью метода MoveToHeaderFooter в DocumentBuilder, что повышает эффективность редактирования документов.
type: docs
weight: 580
url: /ru/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

Перемещает курсор в начало верхнего или нижнего колонтитула в текущем разделе.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Указывает верхний или нижний колонтитул, к которому следует перейти. |

## Примечания

После того, как вы переместили курсор в верхний или нижний колонтитул, вы можете использовать остальную часть[`DocumentBuilder`](../) Методы для изменения содержимого верхнего или нижнего колонтитула.

Если вы хотите создать разные верхние и нижние колонтитулы для первой страницы, вам нужно задать [`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Если вы хотите создать разные верхние и нижние колонтитулы для четных и нечетных страниц, вам нужно задать [`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Использовать[`MoveToSection`](../movetosection/) для перехода от заголовка к основному тексту.

## Примеры

Показывает, как вставить изображение и использовать его в качестве водяного знака.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте изображение в заголовок, чтобы оно было видно на каждой странице.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Разместите изображение в центре страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Показывает, как создавать верхние и нижние колонтитулы в документе с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите, что нам нужны разные верхние и нижние колонтитулы для первой, четной и нечетной страниц.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Создаем заголовки, затем добавляем в документ три страницы для отображения каждого типа заголовков.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Смотрите также

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
