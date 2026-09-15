---
title: "طريقة Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes"
linktitle: "get_IgnoreTextBoxes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes. يحصل على أو يعيّن قيمة منطقية تحدد أن تنسيق المصدر لمحتوى صناديق النص يتم تجاهله إذا تم استخدام وضع KeepSourceFormatting. القيمة الافتراضية هي true في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/importformatoptions/get_ignoretextboxes/
---
## ImportFormatOptions::get_IgnoreTextBoxes method


يحصل على أو يعيّن قيمة منطقية تحدد أن تنسيق المصدر لمحتوى صناديق النص يتم تجاهله إذا تم استخدام وضع [KeepSourceFormatting](../../importformatmode/). القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes() const
```


## أمثلة



يظهر كيفية إدارة تنسيق صندوق النص أثناء إلحاق مستند.
```cpp
// أنشئ مستندًا سيُدرج فيه عقد من مستند آخر.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

builder->Writeln(u"Hello world!");

// أنشئ مستندًا آخر يحتوي على صندوق نص، سنستوردها إلى المستند الأول.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 100);
builder->MoveTo(textBox->get_FirstParagraph());
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Name(u"Courier New");
builder->get_ParagraphFormat()->get_Style()->get_Font()->set_Size(24);
builder->Write(u"Textbox contents");

// عيّن علامة لتحديد ما إذا كان سيتم مسح أو الحفاظ على تنسيق صندوق النص
// أثناء استيرادها إلى مستندات أخرى.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreTextBoxes(ignoreTextBoxes);

// استيراد مربع النص من المستند المصدر إلى المستند الهدف،
// ثم التحقق مما إذا كنا قد حافظنا على تنسيق النص الخاص به.
auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);
auto importedTextBox = System::ExplicitCast<Aspose::Words::Drawing::Shape>(importer->ImportNode(textBox, true));
dstDoc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedTextBox);

if (ignoreTextBoxes)
{
    ASPOSE_ASSERT_EQ(12.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Times New Roman", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}
else
{
    ASPOSE_ASSERT_EQ(24.0, importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Size());
    ASSERT_EQ(u"Courier New", importedTextBox->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
}

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.IgnoreTextBoxes.docx");
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
