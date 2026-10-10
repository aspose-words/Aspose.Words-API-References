---
title: "Aspose::Words::FileFormatInfo::get_HasMacros metod"
linktitle: "get_HasMacros"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatInfo::get_HasMacros metod. Returnerar true om detta dokument innehåller VBA-makron i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Returnerar **true** om detta dokument innehåller VBA-makron.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Exempel



Visar hur man kontrollerar förekomsten av VBA-makron utan att läsa in dokumentet.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## Se även

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
