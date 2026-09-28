---
title: "Метод Aspose::Words::DocumentBuilder::InsertDocumentInline"
linktitle: "InsertDocumentInline"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertDocumentInline. Вставляет документ встроенно в позицию курсора в C++."
type: docs
weight: 33500
url: /ru/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Вставляет документ встроенно в позицию курсора.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Исходный документ для вставки. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Позволяет задавать параметры, влияющие на форматирование результирующего документа. |

### ReturnValue

Первый узел вставленного содержимого.
## Примечания


Этот метод имитирует поведение MS Word, как будто была нажата комбинация CTRL+'A' (выделить всё содержимое), затем CTRL+'C' (скопировать выделенное в буфер) в одном документе, а затем CTRL+'V' (вставить содержимое из буфера) в другом документе.

В отличие от [InsertDocument()](../) этот метод перемещает содержимое абзаца целевого документа, перед которым вставлен исходный документ, в последний абзац вставленного исходного документа. Фактически это означает, что разрыв абзаца последнего вставленного абзаца удаляется.

Примечание: если последний узел исходного документа не является абзацем, то ничего не будет выполнено.

## Примеры



Показывает, как вставить документ встроенно в позицию курсора.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Создайте целевой документ.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Вставьте исходный документ во встроенное положение в целевой документ.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## См. также

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
