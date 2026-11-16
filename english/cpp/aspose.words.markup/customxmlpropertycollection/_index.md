---
title: Aspose::Words::Markup::CustomXmlPropertyCollection class
linktitle: CustomXmlPropertyCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::CustomXmlPropertyCollection class. Represents a collection of custom XML attributes or smart tag properties. To learn more, visit the Structured Document Tags or Content Control documentation article in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


Represents a collection of custom XML attributes or smart tag properties. 
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\> \&) | Adds a property to the collection. |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [Contains](./contains/)(const System::String \&) | Determines whether the collection contains a property with the given name. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOfKey](./indexofkey/)(const System::String \&) | Returns the zero-based index of the specified property in the collection. |
| [Remove](./remove/)(const System::String \&) | Removes a property with the specified name from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes a property at the specified index. |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [idx_get](./idx_get/)(const System::String \&) | Gets a property with the specified name. |
| [idx_get](./idx_get/)(int32_t) | Gets a property at the specified index. |
## Remarks


Items are [CustomXmlProperty](../customxmlproperty/) objects.
## Examples


Shows how to work with smart tag properties to get in depth information about smart tags.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Smart tags.doc"));

// A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
// such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
// In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
// In our input document, there are three objects that Microsoft Word registered as smart tags.
// Smart tags may be nested, so this collection contains more.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag>>()->LINQ_ToArray();

ASSERT_EQ(smartTags->get_Length(), 8);

// The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
// The properties of a "date"-type smart tag contain its year, month, and day.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(properties->get_Count(), 4);

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(enumerator->get_Current()->get_Uri(), u"");
    }
}

// We can also access the properties in various ways, such as a key-value pair.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(properties->idx_get(u"Day")->get_Value(), u"22");
ASSERT_EQ(properties->idx_get(2)->get_Value(), u"2003");
ASSERT_EQ(properties->IndexOfKey(u"Month"), 1);

// Below are three ways of removing elements from the properties collection.
// 1 -  Remove by index:
properties->RemoveAt(3);

ASSERT_EQ(properties->get_Count(), 3);

// 2 -  Remove by name:
properties->Remove(u"Year");

ASSERT_EQ(properties->get_Count(), 2);

// 3 -  Clear the entire collection at once:
properties->Clear();

ASSERT_EQ(properties->get_Count(), 0);
```
## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
