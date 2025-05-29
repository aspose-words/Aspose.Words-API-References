---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NavigationMapLevel HtmlSaveOptions, контролирующее уровни заголовков в экспортах EPUB, MOBI и AZW3. Увеличьте видимость своего контента!
type: docs
weight: 390
url: /ru/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Указывает максимальный уровень заголовков, заполняемых на навигационной карте при экспорте в форматы EPUB, MOBI или AZW3 . Значение по умолчанию:`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Примечания

Карта навигации позволяет агентам пользователя предоставлять простой способ навигации по структуре документа. Обычно точки навигации соответствуют заголовкам в документе. Для того, чтобы заполнить заголовки до уровня**Н** присвоить это значение`NavigationMapLevel`.

По умолчанию заполняются три уровня заголовков: абзацы стилей**Заголовок 1** ,**Заголовок 2** и**Заголовок 3**. Вы можете установить это свойство на значение от 1 до 9, чтобы запросить соответствующий максимальный уровень. Установка его на ноль сократит карту навигации только до корня документа или корней частей документа.

## Примеры

Показывает, как создать оглавление для документов Azw3.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Показывает, как создать оглавление для документов Mobi.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Показывает, как фильтровать заголовки, отображаемые на панели навигации сохраненного документа Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац, который мы форматируем с использованием стиля «Заголовок», может служить заголовком.
// Каждый заголовок может также иметь уровень заголовка, определяемый номером его стиля заголовка.
// Заголовки ниже относятся к уровням 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Читатели epub обычно создают оглавление для своих документов.
// Каждый абзац со стилем «Заголовок» в документе создаст запись в этом оглавлении.
 // Мы можем использовать свойство «NavigationMapLevel» для установки максимального уровня заголовка.
// Читатель Epub не будет добавлять заголовки с уровнем выше указанного нами в таблицу содержания.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// В нашем документе шесть заголовков, два из которых находятся выше уровня 2.
// Содержание этого документа будет состоять из четырех записей.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
