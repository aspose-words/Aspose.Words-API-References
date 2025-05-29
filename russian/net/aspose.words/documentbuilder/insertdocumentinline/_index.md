---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words для .NET
description: С легкостью вставляйте документы в строку с помощью метода InsertDocumentInline в DocumentBuilder, что улучшает рабочий процесс и удобство редактирования документов.
type: docs
weight: 320
url: /ru/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Вставляет документ в позицию курсора.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | Document | Исходный документ для вставки. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующие стили форматирования. |
| importFormatOptions | ImportFormatOptions | Позволяет указать параметры, влияющие на форматирование результирующего документа. |

### Возвращаемое значение

Первый узел вставленного контента.

## Примечания

Этот метод имитирует поведение MS Word, как если бы было нажато CTRL+'A' (выделить все содержимое), затем CTRL+'C' (скопировать выделенное в буфер) внутри одного документа и затем CTRL+'V' (вставить содержимое из буфера) внутри другого документа.

В отличие от[`InsertDocument`](../insertdocument/) этот метод перемещает содержимое абзаца целевого документа, перед которым вставлен исходный документ, в последний абзац вставленного исходного документа. Фактически это означает, что разрыв абзаца последнего вставленного абзаца удаляется.

Обратите внимание: если последний узел исходного документа не является абзацем, то ничего сделано не будет.

## Примеры

Показывает, как вставить документ в позицию курсора.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Создать целевой документ.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Вставьте исходный документ в целевой инлайн.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Смотрите также

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
