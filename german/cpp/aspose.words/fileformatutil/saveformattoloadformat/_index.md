---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat Methode"
linktitle: "SaveFormatToLoadFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat Methode. Konvertiert einen SaveFormat-Wert in einen LoadFormat-Wert, falls möglich, in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Konvertiert einen [SaveFormat](../../saveformat/) Wert in einen [LoadFormat](../../loadformat/) Wert, falls möglich.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Beispiele



Zeigt, wie man ein SaveFormat in das entsprechende LoadFormat konvertiert.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Einige Dateitypen können mit Aspose.Words gespeichert, aber nicht geladen werden.
// Wenn wir versuchen, ein SaveFormat eines solchen Typs in ein LoadFormat zu konvertieren, wird eine Ausnahme ausgelöst.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## Siehe auch

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
