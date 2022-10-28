---
title: Frameset
second_title: Aspose.Words for C++ API Reference
description: Represents a frames page or a single frame on a frames page.
type: docs
weight: 1
url: /cpp/aspose.words.framesets/frameset/
---
## Frameset class


Represents a frames page or a single frame on a frames page.

```cpp
class Frameset : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Gets the collection of child frames and frames pages. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Gets or sets the web page URL or document file name to display in this frame. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Gets or sets a value indicating whether the web page or document file name specified in the [FrameDefaultUrl](./get_framedefaulturl/) property is an external resource the frame is linked with. |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Setter for [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Setter for [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |

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

