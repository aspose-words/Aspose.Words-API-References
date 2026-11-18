---
title: Aspose::Words::Document::set_DefaultTabStop method
linktitle: set_DefaultTabStop
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::set_DefaultTabStop method. Sets the interval (in points) between the default tab stops in C++.'
type: docs
weight: 157000
url: /cpp/aspose.words/document/set_defaulttabstop/
---
## Document::set_DefaultTabStop method


Sets the interval (in points) between the default tab stops.

```cpp
void Aspose::Words::Document::set_DefaultTabStop(double value)
```

## Examples


Shows how to set a custom interval for tab stop positions.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set tab stops to appear every 72 points (1 inch).
builder->get_Document()->set_DefaultTabStop(72);

// Each tab character snaps the text after it to the next closest tab stop position.
builder->Writeln(System::String(u"Hello") + ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + ControlChar::TabChar + u"World!");
```
## See Also

* [TabStopCollection](../../tabstopcollection/)
* [TabStop](../../tabstop/)

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
