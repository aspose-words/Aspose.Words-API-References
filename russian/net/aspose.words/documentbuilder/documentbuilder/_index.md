---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words для .NET
description: Создавайте мощные документы без усилий с DocumentBuilder. Инициализируйте новый экземпляр и оптимизируйте управление документами уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Инициализирует новый экземпляр этого класса.

```csharp
public DocumentBuilder()
```

## Примечания

Создает новый[`DocumentBuilder`](../)объект и прикрепляет его к новому[`Document`](../../document/) объект.

## Примеры

Показывает, как вставлять форматированный текст с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите форматирование шрифта, затем добавьте текст.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Инициализирует новый экземпляр этого класса.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Примечания

Создает новый[`DocumentBuilder`](../)объект и прикрепляет его к новому[`Document`](../../document/) object. Могут быть указаны дополнительные параметры построения документа.

## Примеры

Показывает, как игнорировать форматирование таблицы для содержимого после.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Добавляет содержимое перед таблицей.
// Размер шрифта по умолчанию — 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Изменяет размер шрифта внутри таблицы.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Если ContextTableFormatting имеет значение true, то форматирование таблицы не применяется к содержимому после.
// Если ContextTableFormatting имеет значение false, то форматирование таблицы применяется к содержимому после.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Смотрите также

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Инициализирует новый экземпляр этого класса.

```csharp
public DocumentBuilder(Document doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | Document | The[`Document`](../../document/) объект для присоединения. |

## Примечания

Создает новый[`DocumentBuilder`](../) объект, прикрепляется к указанному[`Document`](../../document/) object. Курсор установлен в начале документа.

## Примеры

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

Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте оглавление для первой страницы документа.
// Настройте таблицу для выбора абзацев с заголовками уровней 1–3.
// Также задайте его записи как гиперссылки, которые перенесут нас
// в место расположения заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Заполните оглавление, добавив абзацы со стилями заголовков.
// Каждый такой заголовок с уровнем от 1 до 3 создаст запись в таблице.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Оглавление — это поле типа, которое необходимо обновить для отображения актуального результата.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Смотрите также

* class [Document](../../document/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Инициализирует новый экземпляр этого класса.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | Document | The[`Document`](../../document/) объект для присоединения. |
| options | DocumentBuilderOptions | Дополнительные возможности процесса создания документа. |

## Примечания

Создает новый[`DocumentBuilder`](../) объект, прикрепляется к указанному[`Document`](../../document/) object. Курсор установлен в начале документа.

## Примеры

Показывает, как игнорировать форматирование таблицы для содержимого после.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Добавляет содержимое перед таблицей.
// Размер шрифта по умолчанию — 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Изменяет размер шрифта внутри таблицы.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Если ContextTableFormatting имеет значение true, то форматирование таблицы не применяется к содержимому после.
// Если ContextTableFormatting имеет значение false, то форматирование таблицы применяется к содержимому после.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Смотрите также

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
