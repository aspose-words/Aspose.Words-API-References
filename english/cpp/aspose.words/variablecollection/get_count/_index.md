---
title: Aspose::Words::VariableCollection::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::VariableCollection::get_Count method. Gets the number of elements contained in the collection in C++.'
type: docs
weight: 18250
url: /cpp/aspose.words/variablecollection/get_count/
---
## VariableCollection::get_Count method


Gets the number of elements contained in the collection.

```cpp
int32_t Aspose::Words::VariableCollection::get_Count()
```

## Examples


Shows how to work with a document's variable collection.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Every document has a collection of key/value pair variables, which we can add items to.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(variables->get_Count(), 3);

// We can display the values of variables in the document body using DOCVARIABLE fields.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(field->get_Result(), u"123 Main St.");

// Assigning values to existing keys will update them.
variables->Add(u"Home address", u"456 Queen St.");

// We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
ASSERT_EQ(field->get_Result(), u"123 Main St.");

field->Update();

ASSERT_EQ(field->get_Result(), u"456 Queen St.");

// Verify that the document variables with a certain name or value exist.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// The collection of variables automatically sorts variables alphabetically by name.
ASSERT_EQ(variables->IndexOfKey(u"Bedrooms"), 0);
ASSERT_EQ(variables->IndexOfKey(u"City"), 1);
ASSERT_EQ(variables->IndexOfKey(u"Home address"), 2);

ASSERT_EQ(variables->idx_get(0), u"3");
ASSERT_EQ(variables->idx_get(u"City"), u"London");

// Enumerate over the collection of variables.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Below are three ways of removing document variables from a collection.
// 1 -  By name:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  By index:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Clear the whole collection at once:
variables->Clear();

ASSERT_EQ(variables->get_Count(), 0);
```
## See Also

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
