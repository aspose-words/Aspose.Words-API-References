---
title: Aspose::Words::ParagraphFormat::get_LinesToDrop method
linktitle: get_LinesToDrop
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_LinesToDrop method. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Examples



Shows how to set the size of a drop cap. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modify the "LinesToDrop" property to designate a paragraph as a drop cap,
// which will turn it into a large capital letter that will decorate the next paragraph.
// Give this property a value of 4 to give the drop cap the height of four text lines.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Reset the "LinesToDrop" property to 0 to turn the next paragraph into an ordinary paragraph.
// The text in this paragraph will wrap around the drop cap.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
