---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars method"
linktitle: "get_KeepLegacyControlChars"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars method. Behält die ursprüngliche Darstellung von Legacy‑Steuerzeichen in C++ bei."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


Behält die ursprüngliche Darstellung von Legacy-Steuerzeichen bei.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Beispiele



Zeigt, wie man Legacy‑Steuerzeichen beim Konvertieren zu .docx unterstützt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Wenn wir das Dokument in ein OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und es dann an die Speichermethode des Dokuments übergeben, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft "KeepLegacyControlChars" auf "true", um beizubehalten
// das Legacy‑Zeichen "ShortDateTime" beim Speichern.
// Setzen Sie die Eigenschaft "KeepLegacyControlChars" auf "false", um zu entfernen
// das Legacy‑Zeichen "ShortDateTime" aus dem Ausgabedokument.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Siehe auch

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
