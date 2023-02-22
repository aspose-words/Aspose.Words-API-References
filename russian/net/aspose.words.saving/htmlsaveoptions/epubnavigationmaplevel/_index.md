---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает максимальный уровень заголовков заполняемых навигационной картой при экспорте в формат IDPF EPUB. Значение по умолчанию3 .
type: docs
weight: 110
url: /ru/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

Указывает максимальный уровень заголовков, заполняемых навигационной картой при экспорте в формат IDPF EPUB. Значение по умолчанию:`3` .

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### Примечания

Карта навигации в формате IDPF EPUB позволяет агентам пользователя обеспечивать простой способ навигации по структуре документа. Обычно точки навигации соответствуют заголовкам в документе. Для заполнения заголовков до уровня **Н** присвоить это значение`EpubNavigationMapLevel`.

По умолчанию заполняются три уровня заголовков: абзацы стилей **Заголовок 1** , **Заголовок 2** и **Заголовок 3**. Вы можете установить для этого свойства значение от 1 до 9, чтобы запросить соответствующий максимальный уровень. Установка его на ноль уменьшит карту навигации только до корня документа или корней частей документа.

### Примеры

Показывает, как фильтровать заголовки, которые появляются на панели навигации сохраненного документа Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац, который мы форматируем с использованием стиля «Заголовок», может служить заголовком.
// У каждого заголовка также может быть уровень заголовка, определяемый номером его стиля заголовка.
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

// Читатели Epub обычно создают оглавление для своих документов.
// Каждый абзац со стилем «Заголовок» в документе создаст запись в этой таблице содержания.
 // Мы можем использовать свойство "EpubNavigationMapLevel", чтобы установить максимальный уровень заголовка.
// Читатель Epub не будет добавлять заголовки с уровнем выше того, который мы указываем в таблицу содержимого.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// Наш документ имеет шесть заголовков, два из которых выше уровня 2.
// В оглавлении этого документа будет четыре записи.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


