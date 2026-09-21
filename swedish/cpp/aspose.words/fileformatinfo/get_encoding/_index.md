---
title: "Aspose::Words::FileFormatInfo::get_Encoding metod"
linktitle: "get_Encoding"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatInfo::get_Encoding metod. Hämtar den upptäckta kodningen om den är tillämplig på det aktuella dokumentformatet. För närvarande upptäcker den kodning endast för HTML‑dokument i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Hämtar den upptäckta kodningen om den är tillämplig på det aktuella dokumentformatet. För närvarande upptäcker den kodning endast för HTML-dokument.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## Exempel



Visar hur man upptäcker kodning i en html‑fil.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Egenskapen Encoding används endast när vi skapar ett FileFormatInfo‑objekt för ett html‑dokument.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Se även

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
