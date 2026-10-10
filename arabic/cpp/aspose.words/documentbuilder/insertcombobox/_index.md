---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertComboBox method. تُدرج حقل نموذج صندوق مركب في الموضع الحالي في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


يدرج حقل نموذج صندوق قائمة منسدلة في الموضع الحالي.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. سيتم قطع القيمة التي تتجاوز 20 حرفًا. |
| items | const System::ArrayPtr\<System::String\>\& | عناصر صندوق القائمة. الحد الأقصى هو 25 عنصرًا. |
| selectedIndex | int32_t | فهرس العنصر المحدد في صندوق القائمة. |

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


يوضح كيفية إدراج حقل نموذج صندوق مركب في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج نموذجًا يطلب من المستخدم اختيار أحد العناصر من القائمة.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## انظر أيضًا

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
