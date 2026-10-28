---
title: Aspose::Words::Layout::LayoutOptions::set_ShowParagraphMarks method
linktitle: set_ShowParagraphMarks
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutOptions::set_ShowParagraphMarks method. Sets indication of whether paragraph marks are rendered. Default is false in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.layout/layoutoptions/set_showparagraphmarks/
---
## LayoutOptions::set_ShowParagraphMarks method


Sets indication of whether paragraph marks are rendered. Default is **false**.

```cpp
void Aspose::Words::Layout::LayoutOptions::set_ShowParagraphMarks(bool value)
```

## Examples


Shows how to show paragraph marks in a rendered output document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
// with a pilcrow (¶) symbol when we render the document.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```
## See Also

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
