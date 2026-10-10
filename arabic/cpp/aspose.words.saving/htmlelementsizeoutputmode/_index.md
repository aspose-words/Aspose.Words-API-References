---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum"
linktitle: "HtmlElementSizeOutputMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enum. يحدد كيف يقوم Aspose.Words بتصدير عرض وارتفاع العناصر إلى HTML و MHTML و EPUB في C++."
type: docs
weight: 58000
url: /ar/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


يحدد كيفية تصدير Aspose.Words لأبعاد العناصر (العرض والارتفاع) إلى HTML أو MHTML و EPUB.

```cpp
enum class HtmlElementSizeOutputMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| الكل | 0 | جميع أحجام العناصر، سواءً بوحدات مطلقة أو نسبية، المحددة في المستند يتم تصديرها. |
| RelativeOnly | 1 | يتم تصدير أحجام العناصر فقط إذا تم تحديدها بوحدات نسبية في المستند. الأحجام الثابتة لا يتم تصديرها في هذا الوضع. سيقوم الوكلاء البصريون بحساب الأحجام المفقودة لجعل تخطيط المستند أكثر طبيعية. |
| None | 2 | أحجام العناصر لا يتم تصديرها. سيقوم الوكلاء البصريون بإنشاء التخطيط تلقائيًا وفقًا للعلاقة بين العناصر. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
