---
title: "Aspose::Words::DocumentBuilder::InsertFootnote метод"
linktitle: "InsertFootnote"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertFootnote метод. Вставляет сноску или концевую сноску в документ в C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Вставляет сноску или концевую сноску в документ.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Указывает, следует ли вставлять сноску или концевую сноску. |
| footnoteText | const System::String\& | Указывает текст сноски. |

### ReturnValue

Возвращает объект сноски, который только что был создан.

## Примеры



Показывает, как ссылаться на текст с помощью сноски и концевой сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте некоторый текст и пометьте его сноской, у которой свойство IsAuto по умолчанию установлено в "true",
// чтобы маркер, видимый в основном тексте, был автоматически пронумерован как "1",
// и сноска появится внизу страницы.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Вставьте ещё текст и пометьте его концевой сноской с пользовательским маркером ссылки,
// который будет использоваться вместо числа "2" и установит "IsAuto" в false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Сноски всегда появляются внизу текста, к которому они относятся,
// поэтому разрыв страницы не повлияет на сноску.
// С другой стороны, концевые сноски всегда находятся в конце документа
// поэтому этот разрыв страницы перенесёт концевую сноску на следующую страницу.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## См. также

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Вставляет сноску или концевую сноску в документ.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Указывает, следует ли вставлять сноску или концевую сноску. |
| footnoteText | const System::String\& | Указывает текст сноски. |
| referenceMark | const System::String\& | Указывает пользовательскую метку ссылки сноски. |

### ReturnValue

Возвращает объект сноски, который только что был создан.

## Примеры



Показывает, как ссылаться на текст с помощью сноски и концевой сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте некоторый текст и пометьте его сноской, у которой свойство IsAuto по умолчанию установлено в "true",
// чтобы маркер, видимый в основном тексте, был автоматически пронумерован как "1",
// и сноска появится внизу страницы.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Вставьте ещё текст и пометьте его концевой сноской с пользовательским маркером ссылки,
// который будет использоваться вместо числа "2" и установит "IsAuto" в false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Сноски всегда появляются внизу текста, к которому они относятся,
// поэтому разрыв страницы не повлияет на сноску.
// С другой стороны, концевые сноски всегда находятся в конце документа
// поэтому этот разрыв страницы перенесёт концевую сноску на следующую страницу.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## См. также

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
