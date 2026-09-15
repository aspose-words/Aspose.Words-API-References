---
title: "Aspose::Words::HeaderFooterCollection فئة"
linktitle: "HeaderFooterCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::HeaderFooterCollection فئة. يوفر وصولًا مكتوبًا إلى عقد HeaderFooter في Section. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


يوفر وصولًا مكتوبًا إلى عقد [HeaderFooter](../headerfooter/) في [Section](../section/). لمعرفة المزيد، زر مقالة الوثائق [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/).

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get_Count](../nodecollection/get_count/)() | يحصل على عدد العقد في المجموعة. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يسترجع [HeaderFooter](../headerfooter/) عند الفهرس المعطى. |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | يسترجع [HeaderFooter](../headerfooter/) من النوع المحدد. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | يربط أو يفك ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة في القسم السابق. |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | يربط أو يفك ربط الرأس أو التذييل المحدد بالرأس أو التذييل المقابل في القسم السابق. |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](./toarray/)() | ينسخ جميع **HeaderFooter**s من المجموعة إلى مصفوفة جديدة من **HeaderFooter**s. |
| static [Type](./type/)() |  |
## ملاحظات


يمكن أن يكون هناك حد أقصى لواحد من [HeaderFooter](../headerfooter/)

من كل [HeaderFooterType](../headerfootertype/) لكل [Section](../section/).

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

## أمثلة



يوضح كيفية إنشاء رأس وتذييل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ رأسًا وأضف فقرةً إليه. النص في تلك الفقرة
// سيظهر في أعلى كل صفحة من هذا القسم، فوق النص الأساسي.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// أنشئ تذييلًا وأضف فقرةً إليه. النص في تلك الفقرة
// سيظهر في أسفل كل صفحة من هذا القسم، تحت النص الأساسي.
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


يوضح كيفية حذف جميع التذييلات من مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// تكرار عبر كل قسم وإزالة التذييلات من جميع الأنواع.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // هناك ثلاثة أنواع من التذييلات والرؤوس.
    // 1 -  "First" رأس/تذييل، الذي يظهر فقط في الصفحة الأولى من القسم.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  "Primary" رأس/تذييل، الذي يظهر في الصفحات الفردية.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  "Even" رأس/تذييل، الذي يظهر في الصفحات الزوجية.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```

## انظر أيضًا

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
