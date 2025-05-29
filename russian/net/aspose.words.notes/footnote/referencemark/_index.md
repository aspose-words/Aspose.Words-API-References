---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words для .NET
description: Настройте свои сноски с помощью свойства ReferenceMark. Легко устанавливайте уникальные маркеры для ясности и организации ваших документов. Улучшите читаемость сегодня!
type: docs
weight: 60
url: /ru/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Получает/устанавливает пользовательский ссылочный знак, который будет использоваться для этой сноски. Значение по умолчанию:**пустая строка** (Empty ), то есть используются автоматически пронумерованные сноски.

```csharp
public string ReferenceMark { get; set; }
```

## Примечания

Если это свойство установлено в**пустая строка** (Empty ) или`нулевой` , затем[`IsAuto`](../isauto/) свойство будет автоматически установлено на`истинный` , если установлено что-либо другое, то[`IsAuto`](../isauto/) будет установлен на`ЛОЖЬ` .

Формат RTF может хранить только 1 символ в качестве пользовательского реперного знака, поэтому при экспорте будет записан только первый символ, остальные будут отброшены.

## Примеры

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте текст и сделайте на него ссылку с помощью сноски. Эта сноска поместит небольшую надстрочную ссылку
// отметьте после текста, на который он ссылается, и создайте запись под основным текстом в нижней части страницы.
// Эта запись будет содержать ссылочный знак сноски и текст ссылки,
// который мы передадим методу "InsertFootnote" конструктора документа.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Если это свойство установлено в значение "true", то ссылочный знак нашей сноски
// будет его индексом среди всех сносок раздела.
// Это первая сноска, поэтому ссылочный знак будет «1».
Assert.True(footnote.IsAuto);

 // Мы можем переместить конструктор документа внутрь сноски, чтобы редактировать ее ссылочный текст.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Мы можем установить пользовательский ссылочный знак, который будет использоваться в сноске вместо ее индексного номера.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Закладка с флагом "IsAuto", установленным в значение true, по-прежнему будет отображать свой реальный индекс
// даже если предыдущие закладки отображали пользовательские контрольные метки, контрольная метка этой закладки будет «3».
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
