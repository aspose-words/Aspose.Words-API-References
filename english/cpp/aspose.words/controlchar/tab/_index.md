---
title: Tab
second_title: Aspose.Words for C++ API Reference
description: 'Tab character: "\x0009" or "\t".'
type: docs
weight: 144
url: /cpp/aspose.words/controlchar/tab/
---
## ControlChar.Tab method


Tab character: "\x0009" or "\t".

```cpp
static System::String & Aspose::Words::ControlChar::Tab()
```


## Examples




Shows how to set a custom interval for tab stop positions. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set tab stops to appear every 72 points (1 inch).
builder->get_Document()->set_DefaultTabStop(72);

// Each tab character snaps the text after it to the next closest tab stop position.
builder->Writeln(String(u"Hello") + ControlChar::Tab() + u"World!");
builder->Writeln(String(u"Hello") + ControlChar::TabChar + u"World!");
```

