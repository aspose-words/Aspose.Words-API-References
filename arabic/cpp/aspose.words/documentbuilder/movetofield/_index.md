---
title: "Aspose::Words::DocumentBuilder::MoveToField طريقة"
linktitle: "MoveToField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::MoveToField طريقة. ينقل المؤشر إلى حقل في المستند في C++."
type: docs
weight: 56000
url: /ar/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


ينقل المؤشر إلى حقل في المستند.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| حقل | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | الحقل الذي سيتم نقل المؤشر إليه. |
| isAfter | bool | عند **true**، ينقل المؤشر ليكون بعد نهاية الحقل. عند **false**، ينقل المؤشر ليكون قبل بداية الحقل. |

## أمثلة



يوضح كيفية نقل مؤشر نقطة إدراج العقدة في DocumentBuilder إلى حقل محدد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج حقلًا باستخدام DocumentBuilder وأضف مجموعة نصية بعده.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// المؤشر في الـ builder حاليًا في نهاية المستند.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// انقل المؤشر إلى الحقل مع تحديد ما إذا كان سيتم وضع المؤشر قبل الحقل أو بعده.
builder->MoveToField(field, moveCursorToAfterTheField);

// لاحظ أن المؤشر خارج الحقل في الحالتين.
// هذا يعني أننا لا نستطيع تعديل الحقل باستخدام الـ builder بهذه الطريقة.
// لتعديل حقل، يمكننا استخدام طريقة MoveTo الخاصة بالـ builder على FieldStart الخاص بالحقل
// أو عقدة FieldSeparator لوضع المؤشر بداخلها.
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
