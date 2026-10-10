---
title: "فئة Aspose::Words::Lists::ListLabel"
linktitle: "ListLabel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Lists::ListLabel. تحدد الخصائص الخاصة بتسمية القائمة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.lists/listlabel/
---
## ListLabel class


يحدد الخصائص الخاصة بتسمية القائمة. لمعرفة المزيد، زر مقالة الوثائق [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLabel : public Aspose::Words::IRunAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Font](./get_font/)() | يحصل على خط تسمية القائمة. |
| [get_LabelString](./get_labelstring/)() | يحصل على تمثيل نصي لتسمية القائمة. |
| [get_LabelValue](./get_labelvalue/)() | يحصل على قيمة رقمية لهذه التسمية. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية استخراج تسميات القوائم لجميع الفقرات التي هي عناصر قائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// ابحث إذا كان لدينا قائمة الفقرات. في مستندنا، تستخدم قائمتنا أرقام عربية عادية،
// التي تبدأ من ثلاثة وتنتهي عند ستة.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // هذا هو النص الذي نحصل عليه عند إخراج هذه العقدة إلى تنسيق نص.
    // سيتم حذف تسميات القوائم في هذا الإخراج النصي. احذف أي أحرف تنسيق الفقرة.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // هذا يحصل على موضع الفقرة في المستوى الحالي للقائمة. إذا كان لدينا قائمة متعددة المستويات،
    // سيخبرنا هذا ما هو الموضع في ذلك المستوى.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // اجمعهما معًا لتضمين تسمية القائمة مع النص في الإخراج.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
