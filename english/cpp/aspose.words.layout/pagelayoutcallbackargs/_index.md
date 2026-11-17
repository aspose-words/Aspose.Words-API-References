---
title: Aspose::Words::Layout::PageLayoutCallbackArgs class
linktitle: PageLayoutCallbackArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::PageLayoutCallbackArgs class. An argument passed into Notify()To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


An argument passed into [Notify()](../ipagelayoutcallback/notify/)To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) documentation article.

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Gets document. |
| [get_Event](./get_event/)() const | Gets event. |
| [get_PageIndex](./get_pageindex/)() | Gets 0-based index of the page in the document this event relates to. Returns negative value if there is no associated page, or if page was removed during reflow. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
