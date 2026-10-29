---
title: Aspose::Words::Framesets::FramesetCollection class
linktitle: FramesetCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Framesets::FramesetCollection class. Represents a collection of instances of the Frameset class. To learn more, visit the Programming with Documents documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class


Represents a collection of instances of the [Frameset](../frameset/) class. 
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class FramesetCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Framesets::Frameset>>
```

## Methods

| Method | Description |
| --- | --- |
| [FramesetCollection](./framesetcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator that iterates through the collection. |
| [get_Count](./get_count/)() | Gets the number of frames or frames pages contained in the collection. |
| [idx_get](./idx_get/)(int32_t) | Gets a frame or frames page at the specified index. |
## Examples


Shows how to access frames on-page.

```cpp
// Document contains several frames with links to other documents.
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Frameset.docx"));

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// We can check the default URL (a web page URL or local document) or if the frame is an external resource.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Change properties for one of our frames.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```
## See Also

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
