---
title: "Aspose::Words::Fonts::EmbeddedFontFormat enum"
linktitle: "EmbeddedFontFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. Specifica il formato di un particolare font incorporato all'interno dell'oggetto FontInfo. Quando si salva un documento su file, vengono scritti solo i font incorporati del formato corrispondente in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Specifica il formato di un particolare font incorporato all'interno dell'oggetto [FontInfo](../fontinfo/). Quando si salva un documento su file, vengono scritti solo i font incorporati del formato corrispondente.

```cpp
enum class EmbeddedFontFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Specifica il formato di file Embedded OpenType (EOT). Questo formato di font incorporati è utilizzato nei file DOC. |
| OpenType | 1 | Specifica il font, incorporato come copia semplice del file font OpenType (TrueType). Questo formato di font incorporati è utilizzato nel formato Open Office XML, inclusi i file DOCX. |


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
