---
title: get_HighlightColor
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the highlight (marker) color.
type: docs
weight: 196
url: /cpp/aspose.words/font/get_highlightcolor/
---
## Font.get_HighlightColor method


Gets or sets the highlight (marker) color.

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Examples




Shows how to format a run of text using its font property. 
```cpp
auto doc = MakeObject<Document>();
auto run = MakeObject<Run>(doc, u"Hello world!");

SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(run);
doc->Save(ArtifactsDir + u"Font.CreateFormattedRun.docx");
```

