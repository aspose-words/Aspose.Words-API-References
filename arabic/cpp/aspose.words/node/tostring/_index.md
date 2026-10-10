---
title: "طريقة Aspose::Words::Node::ToString"
linktitle: "ToString"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::ToString. يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

محتوى العقدة بالتنسيق المحدد.

## أمثلة



يعرض الفرق بين استدعاء طريقتي GetText و ToString على عقدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// ستسترجع GetText النص الظاهر بالإضافة إلى رموز الحقول والأحرف الخاصة.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ستعطينا ToString مظهر المستند إذا تم حفظه بصيغة حفظ محددة.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


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


يصدر محتوى عقدة إلى سلسلة بتنسيق HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// عند استدعائنا طريقة ToString باستخدام التحميل الزائد html SaveFormat،
// يقوم بتحويل محتويات العقدة إلى تمثيلها الخام بصيغة html.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// يمكننا أيضًا تعديل نتيجة هذا التحويل باستخدام كائن SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## انظر أيضًا

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\\<Aspose::Words::Saving::SaveOptions\\>\\& | يحدد الخيارات التي تتحكم في كيفية حفظ العقدة. |

### ReturnValue

محتوى العقدة بالتنسيق المحدد.

## أمثلة



يصدر محتوى عقدة إلى سلسلة بتنسيق HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// عند استدعائنا طريقة ToString باستخدام التحميل الزائد html SaveFormat،
// يقوم بتحويل محتويات العقدة إلى تمثيلها الخام بصيغة html.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// يمكننا أيضًا تعديل نتيجة هذا التحويل باستخدام كائن SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## انظر أيضًا

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
