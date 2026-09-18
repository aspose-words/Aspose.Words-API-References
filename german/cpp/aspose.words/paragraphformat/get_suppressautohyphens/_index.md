---
title: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens Methode"
linktitle: "get_SuppressAutoHyphens"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens Methode. Gibt an, ob der aktuelle Absatz von jeglicher Silbentrennung, die in den Dokumenteneinstellungen in C++ angewendet wird, ausgenommen werden soll."
type: docs
weight: 38000
url: /de/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Gibt an, ob der aktuelle Absatz von jeglicher Silbentrennung, die in den Dokumenteinstellungen angewendet wird, ausgenommen sein soll.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Beispiele



Zeigt, wie man die Silbentrennung für einen Absatz unterdrückt.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Öffnen Sie ein Dokument, das Text mit einer Gebietsschema enthält, das mit dem unseres Wörterbuchs übereinstimmt.
// Wenn wir dieses Dokument in einem festen Seitenformat speichern, wird sein Text silbentrennt.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Wir können die Eigenschaft "SuppressAutoHyphens" auf "true" setzen, um die Silbentrennung zu deaktivieren
// für einen bestimmten Absatz, während sie für den Rest des Dokuments aktiviert bleibt.
// Der Standardwert für diese Eigenschaft ist "false",
// was bedeutet, dass jeder Absatz standardmäßig Silbentrennung verwendet, falls verfügbar.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
