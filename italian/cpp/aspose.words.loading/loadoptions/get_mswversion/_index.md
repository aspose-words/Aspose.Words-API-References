---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion method"
linktitle: "get_MswVersion"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion method. Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito è Word2019 in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito è [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Esempi



Mostra come emulare la procedura di caricamento di una specifica versione di Microsoft Word durante il caricamento del documento.
```cpp
// Per impostazione predefinita, Aspose.Words carica i documenti secondo la specifica di Microsoft Word 2019.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// Questo documento manca dello stile di formattazione del paragrafo predefinito.
// Questo stile predefinito verrà rigenerato quando carichiamo il documento sia con Microsoft Word sia con Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// L'interlinea dello stile avrà questo valore quando viene caricata secondo la specifica di Microsoft Word 2007.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## Vedi anche

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
