---
title: Aspose::Words::ControlChar::TabChar field
linktitle: TabChar
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ControlChar::TabChar field. Tab character: (char)9 or "\t" in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Tab character: (char)9 or "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
```


## Examples



Shows how to set a custom interval for tab stop positions. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set tab stops to appear every 72 points (1 inch).
builder->get_Document()->set_DefaultTabStop(72);

// Each tab character snaps the text after it to the next closest tab stop position.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## See Also

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
