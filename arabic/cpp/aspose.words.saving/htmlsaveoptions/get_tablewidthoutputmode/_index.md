---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode"
linktitle: "get_TableWidthOutputMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode. يتحكم في كيفية تصدير عرض الجداول والصفوف والخلايا إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي All في C++."
type: docs
weight: 47000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


يتحكم في كيفية تصدير عرض الجداول والصفوف والخلايا إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## ملاحظات


في تنسيق HTML، يمكن تحديد عرض عناصر الجدول والصف والخلية (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) إما بوحدات نسبية (نسبة مئوية) أو بوحدات مطلقة. في مستند في Aspose.Words، يمكن أيضًا تحديد عرض الجداول والصفوف والخلايا باستخدام إما وحدات نسبية أو مطلقة.

عند تحويل مستند إلى HTML باستخدام Aspose.Words، قد ترغب في التحكم في كيفية تصدير عرض الجداول والصفوف والخلايا لتؤثر على طريقة عرض المستند الناتج في الوكيل البصري (مثل المتصفح أو العارض).

استخدم هذه الخاصية كمرشح لتحديد قيم عرض الجداول التي يتم تصديرها إلى المستند الهدف. على سبيل المثال، إذا كنت تقوم بتحويل مستند إلى EPUB وتعتزم عرض المستند على جهاز قراءة محمول، فربما ترغب في تجنب تصدير قيم العرض المطلقة. للقيام بذلك تحتاج إلى تحديد وضع الإخراج [RelativeOnly](../../htmlelementsizeoutputmode/) أو [None](../../htmlelementsizeoutputmode/) حتى يتمكن العارض على الجهاز المحمول من تنسيق الجدول ليتناسب مع عرض الشاشة بأفضل شكل ممكن.

## أمثلة



يظهر كيفية الحفاظ على المسافات السلبية في ملف .html الناتج.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج جدولًا بمسافة سلبية، مما سيجعلها تُدفع إلى اليسار متجاوزة حد الصفحة الأيسر.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// أدرج جدولًا بمسافة إيجابية، مما سيجعل الجدول يُدفع إلى اليمين.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// عند حفظ مستند إلى HTML، سيحافظ Aspose.Words فقط على المسافات السلبية
// مثل تلك التي طبقناها على الجدول الأول إذا قمنا بتعيين العلامة "AllowNegativeIndent"
// في كائن SaveOptions الذي سنمرره إلى "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## انظر أيضًا

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
