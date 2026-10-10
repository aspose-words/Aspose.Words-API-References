---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "مربع النص"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::TextBox class. يحدد السمات التي تحدد كيفية عرض النص داخل الشكل. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.drawing/textbox/
---
## TextBox class


يعرف السمات التي تحدد كيفية عرض النص داخل الشكل. لمعرفة المزيد، زر مقالة الوثائق [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class TextBox : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | يكسر الرابط إلى الـ [TextBox](./) التالي. |
| [get_FitShapeToText](./get_fitshapetotext/)() | يحدد ما إذا كان Microsoft Word سيزيد حجم الشكل ليتناسب مع النص. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | يحدد الهامش الداخلي السفلي بالنقاط للشكل. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | يحدد الهامش الداخلي الأيسر بالنقاط للشكل. |
| [get_InternalMarginRight](./get_internalmarginright/)() | يحدد الهامش الداخلي الأيمن بالنقاط للشكل. |
| [get_InternalMarginTop](./get_internalmargintop/)() | يحدد الهامش الداخلي العلوي بالنقاط للشكل. |
| [get_LayoutFlow](./get_layoutflow/)() | يحدد تدفق تخطيط النص داخل الشكل. |
| [get_Next](./get_next/)() | إرجاع أو تعيين [TextBox](./) الذي يمثل الـ [TextBox](./) التالي في تسلسل الأشكال. |
| [get_NoTextRotation](./get_notextrotation/)() | الحصول أو تعيين قيمة منطقية تشير إلى أن نص الـ [TextBox](./) لا يجب أن يدور عندما يتم تدوير الشكل. |
| [get_Parent](./get_parent/)() const | الحصول على الشكل الأب للـ [TextBox](./). |
| [get_Previous](./get_previous/)() | إرجاع [TextBox](./) الذي يمثل الـ [TextBox](./) السابق في تسلسل الأشكال. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | يحدد كيفية التفاف النص داخل الشكل. |
| [get_VerticalAnchor](./get_verticalanchor/)() | يحدد محاذاة النص العمودية داخل الشكل. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | يحدد ما إذا كان هذا [TextBox](./) يمكن ربطه بـ [TextBox](./) الهدف. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | مُعيّن لـ [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## ملاحظات


استخدم خاصية [TextBox](../shape/get_textbox/) للوصول إلى خصائص النص في الشكل. لا تقوم بإنشاء كائنات من فئة [TextBox](./) مباشرةً.

## أمثلة



يوضح كيفية تعيين اتجاه النص داخل مربع النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// انقل مُنشئ المستند إلى داخل مربع النص وأضف نصًا.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتحديد اتجاه محتوى النص في هذا مربع النص.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```


يوضح كيفية جعل مربع النص يغير حجمه ليتناسب بإحكام مع محتوياته.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// طبق هذه القيم على كلا العضوين لجعل الشكل الأب يتناسب
// إحكامًا حول محتوى النص، متجاهلًا الأبعاد التي حددناها.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```


يوضح كيفية تعيين الهوامش الداخلية لمربع النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مربع نص آخر بهوامش محددة.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
