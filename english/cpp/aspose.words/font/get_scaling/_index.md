---
title: Aspose::Words::Font::get_Scaling method
linktitle: get_Scaling
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Scaling method. Gets or sets character width scaling in percent in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Gets or sets character width scaling in percent.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
```


## Examples



Shows how to set horizontal scaling and spacing for characters. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add run of text and increase character width to 150%.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Add run of text and add 1pt of extra horizontal spacing between each character.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Add run of text and bring characters closer together by 1pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
