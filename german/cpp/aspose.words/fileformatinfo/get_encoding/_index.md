---
title: "Aspose::Words::FileFormatInfo::get_Encoding-Methode"
linktitle: "get_Encoding"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatInfo::get_Encoding-Methode. Gibt die erkannte Kodierung zurück, sofern sie für das aktuelle Dokumentformat zutrifft. Derzeit wird die Kodierung nur für HTML‑Dokumente in C++ erkannt."
type: docs
weight: 2000
url: /de/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Liest die erkannte Kodierung, falls sie für das aktuelle Dokumentformat zutrifft. Derzeit wird die Kodierung nur für HTML-Dokumente erkannt.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## Beispiele



Zeigt, wie die Kodierung in einer HTML-Datei erkannt wird.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Die Eigenschaft Encoding wird nur verwendet, wenn wir ein FileFormatInfo‑Objekt für ein HTML‑Dokument erstellen.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Siehe auch

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
