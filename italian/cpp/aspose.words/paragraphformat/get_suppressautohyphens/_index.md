---
title: "metodo Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens"
linktitle: "get_SuppressAutoHyphens"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens metodo. Specifica se il paragrafo corrente deve essere esentato da qualsiasi sillabazione applicata nelle impostazioni del documento in C++."
type: docs
weight: 38000
url: /it/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Specifica se il paragrafo corrente deve essere esentato da qualsiasi sillabazione applicata nelle impostazioni del documento.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Esempi



Mostra come sopprimere la sillabazione per un paragrafo.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Apri un documento contenente testo con una locale corrispondente a quella del nostro dizionario.
// Quando salviamo questo documento in un formato di salvataggio a pagina fissa, il suo testo avrà la sillabazione.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Possiamo impostare la proprietà "SuppressAutoHyphens" su "true" per disabilitare la sillabazione
// per un paragrafo specifico mantenendola abilitata per il resto del documento.
// Il valore predefinito per questa proprietà è "false",
// il che significa che ogni paragrafo, per impostazione predefinita, utilizza la sillabazione se disponibile.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
