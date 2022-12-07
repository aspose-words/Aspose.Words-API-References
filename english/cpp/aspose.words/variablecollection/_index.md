---
title: VariableCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of document variables. To learn more, visit the  documentation article.
type: docs
weight: 937
url: /cpp/aspose.words/variablecollection/
---
## VariableCollection class


A collection of document variables. To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) documentation article.

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Adds a document variable to the collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [Contains](./contains/)(const System::String\&) | Determines whether the collection contains a document variable with the given name. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all variable in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Gets or a sets a document variable by the case-insensitive name. **null** values are not allowed as a right hand side of the assignment and will be replaced by empty string. |
| [idx_get](./idx_get/)(int32_t) | Gets or sets a document variable at the specified index. **null** values are not allowed as a right hand side of the assignment and will be replaced by empty string. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Gets or a sets a document variable by the case-insensitive name. **null** values are not allowed as a right hand side of the assignment and will be replaced by empty string. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Gets or sets a document variable at the specified index. **null** values are not allowed as a right hand side of the assignment and will be replaced by empty string. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Returns the zero-based index of the specified document variable in the collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Removes a document variable with the specified name from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes a document variable at the specified index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarks


Variable names and values are strings.

Variable names are case-insensitive.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
