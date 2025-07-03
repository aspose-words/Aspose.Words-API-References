---
title: Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine method
linktitle: get_MaxCharactersPerLine
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine method. Gets or sets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Gets or sets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Examples



Shows how to set maximum number of characters per line. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Set 30 characters as maximum allowed per one line.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## See Also

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
