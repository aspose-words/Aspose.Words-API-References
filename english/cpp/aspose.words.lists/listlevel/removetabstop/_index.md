---
title: Aspose::Words::Lists::ListLevel::RemoveTabStop method
linktitle: RemoveTabStop
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevel::RemoveTabStop method. Removes tab stop from the list level in C++.'
type: docs
weight: 22500
url: /cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Removes tab stop from the list level.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Examples



Shows how to clear the list level tab stop. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a list with default formatting
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Get the list level and remove its tab stop
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## See Also

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
