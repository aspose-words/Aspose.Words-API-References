---
title: get_SmallCaps
second_title: Aspose.Words for C++ API Reference
description: True if the font is formatted as small capital letters.
type: docs
weight: 469
url: /cpp/aspose.words/font/get_smallcaps/
---
## Font::get_SmallCaps method


True if the font is formatted as small capital letters.

```cpp
bool Aspose::Words::Font::get_SmallCaps()
```


## Examples



Shows how to format a run to display its contents in capitals. 
```cpp
auto doc = MakeObject<Document>();
auto para = System::DynamicCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));

// There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
// 1 -  Set the AllCaps flag to display all characters in regular capitals:
auto run = MakeObject<Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild(run);

para = System::DynamicCast<Paragraph>(para->get_ParentNode()->AppendChild(MakeObject<Paragraph>(doc)));

// 2 -  Set the SmallCaps flag to display all characters in small capitals:
// If a character is lower case, it will appear in its upper case form
// but will have the same height as the lower case (the font's x-height).
// Characters that were in upper case originally will look the same.
run = MakeObject<Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild(run);

doc->Save(ArtifactsDir + u"Font.Caps.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
