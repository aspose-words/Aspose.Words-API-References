---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat metod"
linktitle: "SaveFormatToLoadFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat metod. Konverterar ett SaveFormat‑värde till ett LoadFormat‑värde om möjligt i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Konverterar ett [SaveFormat](../../saveformat/)‑värde till ett [LoadFormat](../../loadformat/)‑värde om möjligt.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Exempel



Visar hur man konverterar ett sparaformat till motsvarande läsformat.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Vissa filtyper kan ha dokument sparade till, men inte lästa från med Aspose.Words.
// Om vi försöker konvertera ett sparaformat av en sådan typ till ett läsformat, kommer ett undantag att kastas.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## Se även

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
