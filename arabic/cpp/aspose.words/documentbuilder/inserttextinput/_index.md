---
title: "Aspose::Words::DocumentBuilder::InsertTextInput method"
linktitle: "InsertTextInput"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertTextInput method. يُدرج حقل نموذج نصي في الموضع الحالي في C++."
type: docs
weight: 49000
url: /ar/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


يدرج حقل نموذج نصي في الموضع الحالي.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. |
| نوع | Aspose::Words::Fields::TextFormFieldType | يحدد نوع حقل النموذج النصي. |
| format | const System::String\& | سلسلة التنسيق المستخدمة لتنسيق قيمة حقل النموذج. |
| fieldValue | const System::String\& | النص الذي سيظهر في الحقل. |
| maxLength | int32_t | الحد الأقصى للطول الذي يمكن للمستخدم إدخاله في حقل النموذج. اضبطه على صفر للحصول على طول غير محدود. |

### ReturnValue

عقدة حقل النموذج التي تم إدراجها للتو.
## ملاحظات


إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة



يظهر كيفية إنشاء حقول النماذج.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// حقول النماذج هي كائنات في المستند يمكن للمستخدم التفاعل معها عن طريق طلب إدخال القيم.
// يمكننا إنشاؤها باستخدام مُنشئ المستند، وفيما يلي طريقتان للقيام بذلك.
// 1 -  إدخال نص أساسي:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  مربع اختيار مع نص توجيه، ونطاق من القيم الممكنة:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```


يوضح كيفية إدراج حقل نموذج إدخال نصي في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج نموذجًا يطلب من المستخدم إدخال نص.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


يوضح كيفية إدراج حقل نموذج إدخال نصي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// أدرج حقل إدخال نصي، سيسمح للمستخدم بالنقر عليه وإدخال النص.
// عيّن بعض النصوص النائبة التي قد يكتب فوقها المستخدم ويمررها
// حد أقصى لطول النص هو 0 لتطبيق عدم وجود حد على محتويات حقل النموذج.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// سيظهر حقل النموذج على شكل وسم HTML "input"، بنوع "text".
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## انظر أيضًا

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
