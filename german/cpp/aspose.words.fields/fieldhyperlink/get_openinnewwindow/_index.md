---
title: "Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow Methode"
linktitle: "get_OpenInNewWindow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow Methode. Liest oder setzt, ob die Zielseite in einem neuen Browserfenster geöffnet werden soll in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fields/fieldhyperlink/get_openinnewwindow/
---
## FieldHyperlink::get_OpenInNewWindow method


Liest oder setzt, ob die Zielseite in einem neuen Browserfenster geöffnet wird.

```cpp
bool Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow()
```


## Beispiele



Zeigt, wie man HYPERLINK-Felder verwendet, um Dokumente im lokalen Dateisystem zu verknüpfen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Wenn wir dieses HYPERLINK-Feld in Microsoft Word anklicken,
// wird das verknüpfte Dokument öffnen und anschließend den Cursor an der angegebenen Lesezeichenposition platzieren.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Wenn wir dieses HYPERLINK-Feld in Microsoft Word anklicken,
// wird das verknüpfte Dokument öffnen und automatisch zum angegebenen iframe scrollen.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Siehe auch

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
