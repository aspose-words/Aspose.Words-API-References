---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars metod"
linktitle: "get_KeepLegacyControlChars"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars metod. Behåller den ursprungliga representationen av äldre kontrolltecken i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


Behåller den ursprungliga representationen av äldre kontrolltecken.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Exempel



Visar hur man stödjer äldre kontrolltecken vid konvertering till .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions‑objekt.
// och sedan skicka den till dokumentets sparningsmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "KeepLegacyControlChars" till "true" för att bevara
// det "ShortDateTime" legacytecknet vid sparande.
// Ställ in egenskapen "KeepLegacyControlChars" till "false" för att ta bort
// det "ShortDateTime" legacytecknet från utdata-dokumentet.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Se även

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
