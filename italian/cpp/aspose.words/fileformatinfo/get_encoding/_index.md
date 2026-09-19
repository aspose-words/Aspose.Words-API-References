---
title: "Metodo Aspose::Words::FileFormatInfo::get_Encoding"
linktitle: "get_Encoding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::FileFormatInfo::get_Encoding. Ottiene la codifica rilevata, se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Ottiene la codifica rilevata, se applicabile al formato del documento corrente. Al momento rileva la codifica solo per i documenti HTML.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## Esempi



Mostra come rilevare la codifica in un file html.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// La proprietà Encoding è usata solo quando creiamo un oggetto FileFormatInfo per un documento html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Vedi anche

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
