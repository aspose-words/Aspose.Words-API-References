---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. Specifica lo stile di un font incorporato all'interno di un oggetto FontInfo in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Specifica lo stile di un font incorporato all'interno di un oggetto [FontInfo](../fontinfo/).

```cpp
enum class EmbeddedFontStyle
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Regolare | 0 | Specifica il carattere incorporato Regular. |
| Grassetto | 1 | Specifica il carattere incorporato Grassetto. |
| Corsivo | 2 | Specifica il carattere incorporato Corsivo. |
| GrassettoCorsivo | 3 | Specifica il carattere incorporato Grassetto-Corsivo. |


## Esempi



Mostra come estrarre un carattere incorporato da un documento e salvarlo nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// I formati dei caratteri incorporati possono essere diversi in altri formati come .doc.
// Dobbiamo conoscere il formato corretto prima di poter estrarre il carattere.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Inoltre, possiamo convertire il formato OpenType incorporato, proveniente da documenti .doc, in OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
