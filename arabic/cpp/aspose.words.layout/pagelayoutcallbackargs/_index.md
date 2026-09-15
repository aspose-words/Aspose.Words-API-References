---
title: "Aspose::Words::Layout::PageLayoutCallbackArgs class"
linktitle: "PageLayoutCallbackArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::PageLayoutCallbackArgs فئة. معامل يُمرّر إلى Notify() لمزيد من المعلومات، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


معامل يُمرّر إلى [Notify()](../ipagelayoutcallback/notify/) لمزيد من المعلومات، زر مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Document](./get_document/)() const | يحصل على المستند. |
| [get_Event](./get_event/)() const | يحصل على الحدث. |
| [get_PageIndex](./get_pageindex/)() | يحصل على الفهرس الصفري للصفحة في المستند الذي يتعلق به هذا الحدث. يُعيد قيمة سالبة إذا لم تكن هناك صفحة مرتبطة، أو إذا أُزيلت الصفحة أثناء إعادة التدفق. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
