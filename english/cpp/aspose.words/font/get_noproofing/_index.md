---
title: get_NoProofing
second_title: Aspose.Words for C++ API Reference
description: True when the formatted characters are not to be spell checked.
type: docs
weight: 365
url: /cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


True when the formatted characters are not to be spell checked.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Examples



Shows how to prevent text from being spell checked by Microsoft Word. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
// We can un-set the "NoProofing" flag to create a portion of text that
// bypasses the spell checker while completely disabling it.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(ArtifactsDir + u"Font.NoProofing.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
