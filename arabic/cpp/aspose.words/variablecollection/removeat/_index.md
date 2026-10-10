---
title: "Aspose::Words::VariableCollection::RemoveAt طريقة"
linktitle: "RemoveAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::VariableCollection::RemoveAt طريقة. يزيل متغيّر مستند عند الفهرس المحدد في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words/variablecollection/removeat/
---
## VariableCollection::RemoveAt method


يزيل متغيّر مستند في الفهرس المحدد.

```cpp
void Aspose::Words::VariableCollection::RemoveAt(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري. |

## أمثلة



يظهر كيفية العمل مع مجموعة متغيّرات المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// كل مستند يحتوي على مجموعة من المتغيّرات على شكل أزواج مفتاح/قيمة، والتي يمكننا إضافة عناصر إليها.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// يمكننا عرض قيم المتغيّرات في جسم المستند باستخدام حقول DOCVARIABLE.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// تعيين القيم للمفاتيح الموجودة سيُحدّثها.
variables->Add(u"Home address", u"456 Queen St.");

// سيتعين علينا بعد ذلك تحديث حقول DOCVARIABLE لضمان عرضها لقيمة محدثة.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// تحقق من وجود متغيّرات المستند ذات اسم أو قيمة معينة.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// مجموعة المتغيّرات تقوم تلقائيًا بترتيب المتغيّرات أبجديًا حسب الاسم.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// تعداد مجموعة المتغيّرات.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// فيما يلي ثلاث طرق لإزالة متغيّرات المستند من مجموعة.
// 1 -  حسب الاسم:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  حسب الفهرس:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  مسح المجموعة بأكملها مرة واحدة:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## انظر أيضًا

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
