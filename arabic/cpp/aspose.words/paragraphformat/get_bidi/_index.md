---
title: "Aspose::Words::ParagraphFormat::get_Bidi طريقة"
linktitle: "get_Bidi"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_Bidi طريقة. يحصل أو يضبط ما إذا كانت هذه فقرة من اليمين إلى اليسار في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


يحصل أو يضبط ما إذا كانت هذه الفقرة من اليمين إلى اليسار.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## ملاحظات


عند **true**، يتم ترتيب المقاطع وغيرها من الكائنات المضمنة في هذه الفقرة من اليمين إلى اليسار.

## أمثلة



يُظهر كيفية إنشاء قوائم متوافقة مع اللغات من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حقل BIDIOUTLINE يرقم الفقرات مثل حقول AUTONUM/LISTNUM،
// ولكنه يظهر فقط عندما يتم تمكين لغة تحرير من اليمين إلى اليسار، مثل العبرية أو العربية.
// الحقل التالي سيعرض ".1"، المكافئ RTL لرقم القائمة "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// أضف حقلين إضافيين من نوع BIDIOUTLINE، سيعرضان ".2" و ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// اضبط محاذاة النص الأفقية لكل فقرة في المستند إلى RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// إذا مكنّا لغة تحرير من اليمين إلى اليسار في Microsoft Word، ستعرض حقولنا أرقامًا.
// وإلا، ستعرض "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


يُظهر كيفية اكتشاف اتجاه نص المستند النصي.
```cpp
// إنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل طريقة تحميل المستند النصي.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// عيّن خاصية "DocumentDirection" إلى "DocumentDirection.Auto" لاكتشاف تلقائيًا
// اتجاه كل فقرة نصية يقوم Aspose.Words بتحميلها من النص العادي.
// ستخزن خاصية "Bidi" لكل فقرة اتجاهها.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// اكتشاف النص العبري كمن اليمين إلى اليسار.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// اكتشاف النص الإنجليزي كمن اليمين إلى اليسار.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
