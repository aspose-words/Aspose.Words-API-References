---
title: Footnote.Footnote
second_title: Справочник по API Aspose.Words для .NET
description: Footnote строитель. Инициализирует экземплярFootnote класс.
type: docs
weight: 10
url: /ru/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Инициализирует экземпляр[`Footnote`](../) класс.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| footnoteType | FootnoteType | А[`FootnoteType`](../footnotetype/) value , указывающее, является ли это сноской или концевой сноской. |

### Примечания

Когда[`Footnote`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../../aspose.words/node/parentnode/) является`нулевой`.

Чтобы добавить[`Footnote`](../) к использованию документаNode) илиNode) в абзаце, в который вы хотите вставить сноску.

### Примеры

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст и ссылаемся на него с помощью сноски. В этой сноске будет помещена небольшая надстрочная ссылка.
// отмечаем после текста, на который он ссылается, и создаем запись под основным текстом внизу страницы.
// Эта запись будет содержать знак ссылки на сноску и текст ссылки,
// который мы передадим методу компоновщика документов "InsertFootnote".
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Если для этого свойства установлено значение «true», то ссылочный знак нашей сноски
// будет его индексом среди всех сносок раздела.
// Это первая сноска, поэтому контрольной отметкой будет «1».
Assert.True(footnote.IsAuto);

 // Мы можем переместить конструктор документа внутрь сноски, чтобы редактировать ссылочный текст.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Мы можем установить собственный ссылочный знак, который будет использоваться в сноске вместо порядкового номера.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Закладка с флагом «IsAuto», установленным в true, все равно будет показывать свой реальный индекс
// даже если предыдущие закладки отображают пользовательские метки, метка этой закладки будет «3».
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../footnote/)
* сборка [Aspose.Words](../../../)


