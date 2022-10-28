---
title: get_Spacing
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the spacing (in points) between characters .
type: docs
weight: 495
url: /cpp/aspose.words/font/get_spacing/
---
## Font.get_Spacing method


Returns or sets the spacing (in points) between characters .

```cpp
double Aspose::Words::Font::get_Spacing()
```


## Examples




Shows how to set horizontal scaling and spacing for characters. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add run of text and increase character width to 150%.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Add run of text and add 1pt of extra horizontal spacing between each character.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Add run of text and bring characters closer together by 1pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(ArtifactsDir + u"Font.ScalingSpacing.docx");
```

