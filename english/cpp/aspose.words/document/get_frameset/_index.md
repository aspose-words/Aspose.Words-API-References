---
title: Aspose::Words::Document::get_Frameset method
linktitle: get_Frameset
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_Frameset method. Returns a Frameset instance if this document represents a frames page in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words/document/get_frameset/
---
## Document::get_Frameset method


Returns a [Frameset](./) instance if this document represents a frames page.

```cpp
System::SharedPtr<Aspose::Words::Framesets::Frameset> Aspose::Words::Document::get_Frameset() const
```


## Examples



Shows how to access frames on-page. 
```cpp
// Document contains several frames with links to other documents.
auto doc = MakeObject<Document>(MyDir + u"Frameset.docx");

// We can check the default URL (a web page URL or local document) or if the frame is an external resource.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
          doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Change properties for one of our frames.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(
    u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## See Also

* Class [Frameset](../../../aspose.words.framesets/frameset/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
