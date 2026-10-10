---
title: "Aspose::Words::TabStopCollection::RemoveByPosition method"
linktitle: "RemoveByPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabStopCollection::RemoveByPosition method. يزيل علامة تبويب في الموضع المحدد من المجموعة في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


يزيل علامة تبويب عند الموضع المحدد من المجموعة.

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| position | double | الموضع (بالنقاط) لعلامة التبويب التي سيتم إزالتها. |

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

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
