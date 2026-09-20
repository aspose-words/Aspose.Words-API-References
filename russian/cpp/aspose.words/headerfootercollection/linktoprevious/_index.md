---
title: "Метод Aspose::Words::HeaderFooterCollection::LinkToPrevious"
linktitle: "LinkToPrevious"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::HeaderFooterCollection::LinkToPrevious. Связывает или разрывает связь указанного заголовка или нижнего колонтитула с соответствующим заголовком или нижним колонтитулом в предыдущем разделе в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


Связывает или разрывает связь указанного заголовка или нижнего колонтитула с соответствующим заголовком или нижним колонтитулом в предыдущем разделе.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Значение [HeaderFooterType](../../headerfootertype/), которое указывает заголовок или нижний колонтитул для связывания/разрыва связи. |
| isLinkToPrevious | bool | **true** — чтобы связать заголовок или нижний колонтитул с предыдущим разделом; **false** — чтобы разорвать связь. |
## Примечания


Если заголовок или нижний колонтитул указанного типа не существует, он создаётся автоматически.

## Примеры



Показывает, как связывать заголовки и нижние колонтитулы между разделами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Перейдите к первому разделу и создайте заголовок и нижний колонтитул. По умолчанию,
// заголовок и нижний колонтитул будут отображаться только на страницах того раздела, в котором они находятся.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Мы можем связать заголовки/нижние колонтитулы раздела с заголовками/нижними колонтитулами предыдущего раздела
// чтобы связанный раздел отображал заголовки/нижние колонтитулы связанного раздела.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Каждый раздел по‑прежнему будет иметь свои собственные объекты заголовка/нижнего колонтитула. Когда мы связываем разделы,
// связывающий раздел будет отображать заголовки/нижние колонтитулы связанного раздела, сохраняя свои собственные.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Свяжите заголовки/нижние колонтитулы третьего раздела с заголовками/нижними колонтитулами второго раздела.
// Второй раздел уже связан с заголовками/нижними колонтитулами первого раздела,
// поэтому связывание со вторым разделом создаст цепочку связей.
// Первый, второй и теперь третий разделы будут все отображать заголовки первого раздела.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Мы можем разорвать связь заголовков/нижних колонтитулов предыдущего раздела, передавая \"false\" при вызове метода LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Мы также можем выбрать только определённый тип заголовка/нижнего колонтитула для связывания с помощью этого метода.
// Третий раздел теперь будет иметь такой же нижний колонтитул, как у второго и первого разделов, но не будет иметь тот же заголовок.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Заголовки/нижние колонтитулы первого раздела не могут связываться ни с чем, потому что предыдущего раздела нет.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Все заголовки/нижние колонтитулы второго раздела связаны с заголовками/нижними колонтитулами первого раздела.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// В третьем разделе только нижний колонтитул связан с нижним колонтитулом первого раздела через второй раздел.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## См. также

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


Связывает или разрывает связь всех заголовков и нижних колонтитулов с соответствующими заголовками и нижними колонтитулами в предыдущем разделе.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** чтобы связать заголовки и нижние колонтитулы с предыдущим разделом; **false** чтобы разорвать связь. |
## Примечания


Если какой-либо из заголовков или нижних колонтитулов не существует, они создаются автоматически.

## Примеры



Показывает, как связывать заголовки и нижние колонтитулы между разделами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Перейдите к первому разделу и создайте заголовок и нижний колонтитул. По умолчанию,
// заголовок и нижний колонтитул будут отображаться только на страницах того раздела, в котором они находятся.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Мы можем связать заголовки/нижние колонтитулы раздела с заголовками/нижними колонтитулами предыдущего раздела
// чтобы связанный раздел отображал заголовки/нижние колонтитулы связанного раздела.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Каждый раздел по‑прежнему будет иметь свои собственные объекты заголовка/нижнего колонтитула. Когда мы связываем разделы,
// связывающий раздел будет отображать заголовки/нижние колонтитулы связанного раздела, сохраняя свои собственные.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Свяжите заголовки/нижние колонтитулы третьего раздела с заголовками/нижними колонтитулами второго раздела.
// Второй раздел уже связан с заголовками/нижними колонтитулами первого раздела,
// поэтому связывание со вторым разделом создаст цепочку связей.
// Первый, второй и теперь третий разделы будут все отображать заголовки первого раздела.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Мы можем разорвать связь заголовков/нижних колонтитулов предыдущего раздела, передавая \"false\" при вызове метода LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Мы также можем выбрать только определённый тип заголовка/нижнего колонтитула для связывания с помощью этого метода.
// Третий раздел теперь будет иметь такой же нижний колонтитул, как у второго и первого разделов, но не будет иметь тот же заголовок.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Заголовки/нижние колонтитулы первого раздела не могут связываться ни с чем, потому что предыдущего раздела нет.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Все заголовки/нижние колонтитулы второго раздела связаны с заголовками/нижними колонтитулами первого раздела.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// В третьем разделе только нижний колонтитул связан с нижним колонтитулом первого раздела через второй раздел.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## См. также

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
