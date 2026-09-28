---
title: "Конструктор Aspose::Words::HeaderFooter::HeaderFooter"
linktitle: "HeaderFooter"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::HeaderFooter::HeaderFooter. Создаёт новый верхний или нижний колонтитул указанного типа в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


Создаёт новый заголовок или нижний колонтитул указанного типа.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| док | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Документ‑владелец. |
| headerFooterType | Aspose::Words::HeaderFooterType | Значение [HeaderFooterType](../get_headerfootertype/), определяющее тип верхнего или нижнего колонтитула. |
## Примечания


Когда создаётся [HeaderFooter](../), он принадлежит указанному документу, но ещё не является частью документа, и [ParentNode](../../node/get_parentnode/) имеет значение **null**.

Чтобы добавить [HeaderFooter](../) к [Section](../../section/) используйте [InsertAfter1()</see>, <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../), либо свойство и методы [HeadersFooters](../../section/get_headersfooters/) [Add()](../), [Insert()](../).

## Примеры



Показывает, как создать заголовок и нижний колонтитул.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте заголовок и добавьте к нему абзац. Текст в этом абзаце
// будет отображаться в верхней части каждой страницы этого раздела, над основным текстом.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Создайте нижний колонтитул и добавьте к нему абзац. Текст в этом абзаце
// будет отображаться в нижней части каждой страницы этого раздела, под основным текстом.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## См. также

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
