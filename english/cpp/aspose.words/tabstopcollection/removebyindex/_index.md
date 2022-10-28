---
title: RemoveByIndex
second_title: Aspose.Words for C++ API Reference
description: Removes a tab stop at the specified index from the collection.
type: docs
weight: 131
url: /cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method


Removes a tab stop at the specified index from the collection.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection of tab stops. |

## Examples




Shows how to select a tab stop in a document by its index and remove it. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(ConvertUtil::MillimeterToPoint(30), TabAlignment::Left, TabLeader::Dashes);
tabStops->Add(ConvertUtil::MillimeterToPoint(60), TabAlignment::Left, TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// Remove the first tab stop.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(ArtifactsDir + u"TabStopCollection.RemoveByIndex.docx");
```

