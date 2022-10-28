---
title: PageLayoutCallbackArgs
second_title: Aspose.Words for C++ API Reference
description: An argument passed into Notify()
type: docs
weight: 40
url: /cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


An argument passed into [Notify()](../ipagelayoutcallback/notify/)

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Gets document. |
| [get_Event](./get_event/)() const | Gets event. |
| [get_PageIndex](./get_pageindex/)() | Gets 0-based index of the page in the document this event relates to. Returns negative value if there is no associated page, or if page was removed during reflow. |
