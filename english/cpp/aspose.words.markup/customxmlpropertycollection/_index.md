---
title: CustomXmlPropertyCollection
second_title: Aspose.Words for C++ API Reference
description: Represents a collection of custom XML attributes or smart tag properties. To learn more, visit the  documentation article.
type: docs
weight: 66
url: /cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


Represents a collection of custom XML attributes or smart tag properties. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/structured-document-tags-or-content-control/) documentation article.

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\>\&) | Adds a property to the collection. |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [Contains](./contains/)(const System::String\&) | Determines whether the collection contains a property with the given name. |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Gets a property with the specified name. |
| [idx_get](./idx_get/)(int32_t) | Gets a property at the specified index. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Returns the zero-based index of the specified property in the collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Removes a property with the specified name from the collection. |
| [RemoveAt](./removeat/)(int32_t) | Removes a property at the specified index. |
| static [Type](./type/)() |  |
## Remarks


Items are [CustomXmlProperty](../customxmlproperty/) objects.

## Examples



Shows how to work with smart tag properties to get in depth information about smart tags. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Smart tags.doc");

// A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
// such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
// In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
// In our input document, there are three objects that Microsoft Word registered as smart tags.
// Smart tags may be nested, so this collection contains more.
ArrayPtr<SharedPtr<SmartTag>> smartTags = doc->GetChildNodes(NodeType::SmartTag, true)->LINQ_OfType<SharedPtr<SmartTag>>()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
// The properties of a "date"-type smart tag contain its year, month, and day.
SharedPtr<CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << "Property name: " << enumerator->get_Current()->get_Name() << ", value: " << enumerator->get_Current()->get_Value() << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// We can also access the properties in various ways, such as a key-value pair.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Below are three ways of removing elements from the properties collection.
// 1 -  Remove by index:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Remove by name:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Clear the entire collection at once:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words](../../)
