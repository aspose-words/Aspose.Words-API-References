---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault طريقة"
linktitle: "get_TextInputDefault"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault طريقة. يحصل أو يضبط السلسلة الافتراضية أو تعبير حسابي لحقل نموذج نصي في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


يحصل على أو يضبط السلسلة الافتراضية أو تعبير الحساب لحقل نموذج نصي.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## ملاحظات


يعتمد معنى هذه الخاصية على قيمة الخاصية [TextInputType](../get_textinputtype/).

عندما تكون [TextInputType](../get_textinputtype/) هي [Regular](../../textformfieldtype/) أو [Number](../../textformfieldtype/)، تحدد هذه السلسلة السلسلة الافتراضية لحقل النموذج النصي. هذه السلسلة هي المحتوى الذي سيعرضه Microsoft Word في المستند عندما يكون حقل النموذج فارغًا.

عندما تكون [TextInputType](../get_textinputtype/) هي [Calculated](../../textformfieldtype/)، تحتفظ هذه السلسلة بالتعبير الذي سيُحسب. يجب أن يكون التعبير صيغة صالحة وفقًا لمتطلبات حقول الصيغ في Microsoft Word. عندما تقوم بتعيين تعبير جديد باستخدام هذه الخاصية، تقوم Aspose.Words بحساب نتيجة الصيغة تلقائيًا وتدرجها في حقل النموذج.

يتيح Microsoft Word سلاسل نصية بحد أقصى 255 حرفًا.
## انظر أيضًا

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
