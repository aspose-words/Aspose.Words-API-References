---
title: Contains
second_title: Aspose.Words for C++ API Reference
description: Determines whether the collection contains a document variable with the given name.
type: docs
weight: 79
url: /cpp/aspose.words/variablecollection/contains/
---
## VariableCollection::Contains method


Determines whether the collection contains a document variable with the given name.

```cpp
bool Aspose::Words::VariableCollection::Contains(const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Case-insensitive name of the document variable to locate. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.

## Examples



Shows how to work with a document's variable collection. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<VariableCollection> variables = doc->get_Variables();

// Every document has a collection of key/value pair variables, which we can add items to.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// We can display the values of variables in the document body using DOCVARIABLE fields.
auto builder = MakeObject<DocumentBuilder>(doc);
auto field = System::DynamicCast<FieldDocVariable>(builder->InsertField(FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Assigning values to existing keys will update them.
variables->Add(u"Home address", u"456 Queen St.");

// We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Verify that the document variables with a certain name or value exist.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any([](auto v) { return v.get_Value() == u"London"; }));

// The collection of variables automatically sorts variables alphabetically by name.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

// Enumerate over the collection of variables.
{
    SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<String, String>>> enumerator =
        doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << "Name: " << enumerator->get_Current().get_Key() << ", Value: " << enumerator->get_Current().get_Value() << std::endl;
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

ASSERT_EQ(0, variables->get_Count());
```

## See Also

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
