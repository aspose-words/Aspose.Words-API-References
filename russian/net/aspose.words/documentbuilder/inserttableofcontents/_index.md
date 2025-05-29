---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words для .NET
description: Легко улучшайте свои документы с помощью метода InsertTableOfContents в DocumentBuilder, добавляя динамическое оглавление для легкой навигации и улучшенной организации.
type: docs
weight: 500
url: /ru/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Вставляет поле TOC (оглавление) в документ.

```csharp
public Field InsertTableOfContents(string switches)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| switches | String | Поле TOC переключается. |

## Примечания

Этот метод вставляет поле TOC (оглавление) в документ в текущей позиции x000d.

Оглавление в документе Word может быть построено несколькими способами и отформатировано с использованием различных опций. Способ построения и отображения таблицы в Microsoft Word контролируется переключателями полей.

Самый простой способ указать переключатели — вставить и настроить таблицу содержимого в документ Word с помощью меню Вставка-&gt;Ссылка-&gt;Указатель и таблицы, , затем включить отображение кодов полей, чтобы увидеть переключатели. Вы можете нажать Alt+F9 в Microsoft Word, чтобы включить или выключить отображение кодов полей.

Например, после создания оглавления в документ вставляется следующее поле :**{ TOC \o "1-3" \h \z \u }** . Вы можете скопировать**\о "1-3" \ч \з \u** и использовать его в качестве параметра переключателя.

Обратите внимание, что`InsertTableOfContents` только вставит поле TOC, но фактически не построит оглавление. Оглавление строится Microsoft Word при обновлении поля.

Если вы вставите оглавление с помощью этого метода, а затем откроете файл в Microsoft Word, вы не увидите оглавление, поскольку поле TOC еще не обновлено.

В Microsoft Word поля не обновляются автоматически при открытии документа, , но вы можете обновить поля в документе в любое время, нажав клавишу F9.

## Примеры

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
