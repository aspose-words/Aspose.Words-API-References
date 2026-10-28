---
title: Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreShapes method
linktitle: set_IgnoreShapes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreShapes method. Sets a boolean value indicating either to ignore shapes within a text.The default value is false in C++.'
type: docs
weight: 27500
url: /cpp/aspose.words.replacing/findreplaceoptions/set_ignoreshapes/
---
## FindReplaceOptions::set_IgnoreShapes method


Sets a boolean value indicating either to ignore shapes within a text.

The default value is **false**.

```cpp
void Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreShapes(bool value)
```

## Examples


Shows how to ignore shapes while replacing text.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(ShapeType::Balloon, static_cast<double>(200), static_cast<double>(200));
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ((u"Lorem ipsum dolor sit amet, consectetur adipiscing elit."), builder->get_Document()->GetText().Trim());
```
## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
