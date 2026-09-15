---
title: "طريقة Aspose::Words::ParagraphFormat::get_TabStops"
linktitle: "get_TabStops"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_TabStops. يحصل على مجموعة علامات التبويب المخصصة المعرفة لهذا الكائن في C++."
type: docs
weight: 40000
url: /ar/cpp/aspose.words/paragraphformat/get_tabstops/
---
## ParagraphFormat::get_TabStops method


يحصل على مجموعة نقاط التبويب المخصصة المعرفة لهذا الكائن.

```cpp
System::SharedPtr<Aspose::Words::TabStopCollection> Aspose::Words::ParagraphFormat::get_TabStops()
```


## أمثلة



يظهر كيفية تعديل موضع موضع التبويب الأيمن في الفقرات المتعلقة بـ TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// تكرار عبر جميع الفقرات ذات الأنماط المستندة إلى نتائج TOC؛ هذا أي نمط بين TOC و TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // احصل على أول تبويب مستخدم في هذه الفقرة، يجب أن يكون هذا التبويب المستخدم لمحاذاة أرقام الصفحات.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // استبدل أول تبويب افتراضي، موضع التبويب، بموضع تبويب مخصّص.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## انظر أيضًا

* Class [TabStopCollection](../../tabstopcollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
