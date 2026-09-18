---
title: "Aspose::Words::Loading::LoadOptions::get_Encoding Methode"
linktitle: "get_Encoding"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_Encoding Methode. Liest oder setzt die Kodierung, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung nicht im Dokument angegeben ist. Kann null sein. Standard ist null in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Liest oder setzt die Kodierung, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. Kann **null** sein. Standard ist **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Hinweise


Diese Eigenschaft wird nur beim Laden von HTML-, TXT- oder CHM-Dokumenten verwendet.

Wenn im Dokument keine Kodierung angegeben ist und diese Eigenschaft **null** ist, versucht das System, die Kodierung automatisch zu erkennen.

## Beispiele



Zeigt, wie die Kodierung festgelegt wird, mit der ein Dokument geöffnet wird.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Laden Sie das Dokument, indem Sie das LoadOptions-Objekt übergeben, und überprüfen Sie anschließend den Inhalt des Dokuments.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
