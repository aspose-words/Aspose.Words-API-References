---
title: "فئة Aspose::Words::TabStop"
linktitle: "TabStop"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::TabStop. تمثّل علامة تبويب مخصصة واحدة. كائن TabStop هو عضو في مجموعة TabStopCollection. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 68000
url: /ar/cpp/aspose.words/tabstop/
---
## TabStop class


تمثّل علامة تبويب مخصصة واحدة. كائن [TabStop](./) هو عضو في مجموعة [TabStopCollection](../tabstopcollection/). لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | يقارن مع [TabStop](./) المحدد. |
| [get_Alignment](./get_alignment/)() const | يحصل أو يضبط محاذاة النص عند هذا موضع التبويب. |
| [get_IsClear](./get_isclear/)() | يرجع **true** إذا كان هذا موضع التبويب يمسح أي مواضع تبويب موجودة في هذا الموضع. |
| [get_Leader](./get_leader/)() const | يحصل أو يضبط نوع خط القائد المعروض تحت حرف التبويب. |
| [get_Position](./get_position/)() | يحصل على موضع موضع التبويب بالنقاط. |
| [GetHashCode](./gethashcode/)() const override | يحسب قيمة التجزئة لهذا الكائن. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | دالة ضبط لـ [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | دالة ضبط لـ [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| static [Type](./type/)() |  |
## ملاحظات


عادةً، يحدد موضع التبويب موقعًا يوجد فيه موضع تبويب. ولكن لأن مواضع التبويب يمكن أن تُورّث من الأنماط الأصلية، قد يكون من الضروري أن يحدد الكائن الفرعي صراحةً أنه لا يوجد موضع تبويب في موقع معين. لمسح موضع تبويب موروث في موقع معين، أنشئ كائنًا من نوع [TabStop](./) واضبط [Alignment](./get_alignment/) إلى [Clear](../tabalignment/).

لمزيد من المعلومات راجع [TabStopCollection](../tabstopcollection/).

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
