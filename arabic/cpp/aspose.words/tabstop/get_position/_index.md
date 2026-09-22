---
title: "طريقة Aspose::Words::TabStop::get_Position"
linktitle: "get_Position"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TabStop::get_Position. يحصل على موضع الوقفة بالنقاط في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/tabstop/get_position/
---
## TabStop::get_Position method


يحصل على موضع موضع التبويب بالنقاط.

```cpp
double Aspose::Words::TabStop::get_Position()
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

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
