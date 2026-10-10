---
title: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces. تسمح بتحديد كيفية التعرف على عناصر القوائم المرقمة عند استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هي true في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


يسمح بتحديد كيفية التعرف على عناصر القوائم المرقمة عندما يتم استيراد المستند من تنسيق نص عادي. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## ملاحظات


إذا تم تعيين هذا الخيار إلى **false**، فإن خوارزمية التعرف على القوائم تكتشف فقرات القوائم عندما تنتهي أرقام القوائم إما بنقطة أو قوس إغلاق أو رموز تعداد (مثل \"•\", \"*\", \"-\" أو \"o\").

إذا تم تعيين هذا الخيار إلى **true**، تُستخدم المسافات البيضاء أيضًا كفواصل لأرقام القوائم: خوارزمية التعرف على القوائم لتعداد النمط العربي (1., 1.1.2.) تستخدم كلًا من المسافات البيضاء ورمز النقطة (\".\").

## أمثلة



يوضح كيفية اكتشاف القوائم عند تحميل مستندات نصية عادية.
```cpp
// أنشئ مستند نص عادي في سلسلة يحتوي على أربعة أجزاء منفصلة يمكننا تفسيرها كقوائم،
// مع فواصل مختلفة. عند تحميل المستند النصي إلى كائن \"Document\"،
// ستقوم Aspose.Words دائمًا باكتشاف القوائم الثلاث الأولى وستضيف كائن \"List\"
// لكل منها إلى خاصية \"Lists\" في المستند.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// إنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل طريقة تحميل المستند النصي.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// قم بتعيين خاصية \"DetectNumberingWithWhitespaces\" إلى \"true\" لاكتشاف العناصر المرقمة
// مع فواصل مسافات بيضاء، مثل القائمة الرابعة في مستندنا، كقوائم.
// قد يؤدي ذلك أيضًا إلى اكتشاف الفقرات التي تبدأ بأرقام على أنها قوائم بشكل خاطئ.
// قم بتعيين خاصية \"DetectNumberingWithWhitespaces\" إلى \"false\"
// لعدم إنشاء قوائم من العناصر المرقمة التي تستخدم فواصل مسافات بيضاء.
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
```

## انظر أيضًا

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
