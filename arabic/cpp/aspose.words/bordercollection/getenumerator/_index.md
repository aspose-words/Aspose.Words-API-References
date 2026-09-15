---
title: "Aspose::Words::BorderCollection::GetEnumerator method"
linktitle: "GetEnumerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BorderCollection::GetEnumerator. تُرجع كائن عدّاد يمكن استخدامه للتنقل عبر جميع الحدود في المجموعة في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع الحدود في المجموعة.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## أمثلة



يوضح كيفية التنقل عبر وتعديل جميع الحدود في كائن تنسيق الفقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتكوين إعدادات تنسيق الفقرة للمنشئ لإنشاء حد موجي أخضر على جميع الجوانب.
System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> enumerator = borders->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Border> border = enumerator->get_Current();
        border->set_Color(System::Drawing::Color::get_Green());
        border->set_LineStyle(Aspose::Words::LineStyle::Wave);
        border->set_LineWidth(3);
    }
}

// أدرج فقرة. ستحدد إعدادات الحدود الخاصة بنا مظهر حدها.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## انظر أيضًا

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
