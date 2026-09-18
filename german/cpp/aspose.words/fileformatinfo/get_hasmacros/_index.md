---
title: "Aspose::Words::FileFormatInfo::get_HasMacros‑Methode"
linktitle: "get_HasMacros"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatInfo::get_HasMacros-Methode. Gibt true zurück, wenn dieses Dokument VBA‑Makros in C++ enthält."
type: docs
weight: 3500
url: /de/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Gibt **true** zurück, wenn dieses Dokument VBA‑Makros enthält.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Beispiele



Zeigt, wie man das Vorhandensein von VBA‑Makros prüft, ohne das Dokument zu laden.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## Siehe auch

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
