---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion Methode"
linktitle: "get_MswVersion"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion Methode. Ermöglicht die Angabe, dass der Dokument-Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist Word2019 in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Ermöglicht die Angabe, dass der Dokument-Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Beispiele



Zeigt, wie beim Laden eines Dokuments das Ladevorgang einer bestimmten Microsoft‑Word‑Version emuliert werden kann.
```cpp
// Standardmäßig lädt Aspose.Words Dokumente gemäß der Microsoft‑Word‑2019‑Spezifikation.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// Dieses Dokument fehlt der standardmäßige Absatzformatierungsstil.
// Dieser Standardstil wird wiederhergestellt, wenn wir das Dokument entweder mit Microsoft Word oder Aspose.Words laden.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// Der Zeilenabstand des Stils hat diesen Wert, wenn er nach der Microsoft‑Word‑2007‑Spezifikation geladen wird.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## Siehe auch

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
