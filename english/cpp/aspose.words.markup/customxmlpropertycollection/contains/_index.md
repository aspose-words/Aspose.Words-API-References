---
title: Contains
second_title: Aspose.Words for C++ API Reference
description: Determines whether the collection contains a property with the given name.
type: docs
weight: 40
url: /cpp/aspose.words.markup/customxmlpropertycollection/contains/
---
## CustomXmlPropertyCollection::Contains method


Determines whether the collection contains a property with the given name.

```cpp
bool Aspose::Words::Markup::CustomXmlPropertyCollection::Contains(const System::String &name)
```


| Parameter | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Case-sensitive name of the property to locate. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

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

* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
