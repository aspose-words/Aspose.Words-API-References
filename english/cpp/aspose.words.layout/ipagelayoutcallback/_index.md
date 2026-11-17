---
title: Aspose::Words::Layout::IPageLayoutCallback interface
linktitle: IPageLayoutCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::IPageLayoutCallback interface. Implement this interface if you want to have your own custom method called during build and rendering of page layout model in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Implement this interface if you want to have your own custom method called during build and rendering of page layout model.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | This is called to notify of layout build and rendering progress. |
| static [Type](./type/)() |  |
## Remarks


The primary use for this interface is to allow application code to abort build process.

It is possible to build page layout model for only a few pages at start of the document then abort process and render only what has been built already.

Note, however, that rendering results may not match what would be rendered for each page if process would have finished.

This technique may not work for every document or may fail completely.

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
