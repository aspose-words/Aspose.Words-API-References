---
title: GetIndexByPosition
second_title: Aspose.Words for C++ API Reference
description: Gets the index of a tab stop with the specified position in points.
type: docs
weight: 92
url: /cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Gets the index of a tab stop with the specified position in points.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Examples



Shows how to look up a position to see if a tab stop exists there and obtain its index. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Add a tab stop at a position of 30mm.
tabStops->Add(ConvertUtil::MillimeterToPoint(30), TabAlignment::Left, TabLeader::Dashes);

// A result of "0" returned by "GetIndexByPosition" confirms that a tab stop
// at 30mm exists in this collection, and it is at index 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(ConvertUtil::MillimeterToPoint(30)));

// A "-1" returned by "GetIndexByPosition" confirms that
// there is no tab stop in this collection with a position of 60mm.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(ConvertUtil::MillimeterToPoint(60)));
```

## See Also

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
