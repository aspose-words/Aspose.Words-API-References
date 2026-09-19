---
title: "Aspose::Words::Fields::FieldHyperlink::get_IsImageMap metodo"
linktitle: "get_IsImageMap"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldHyperlink::get_IsImageMap metodo. Ottiene o imposta se aggiungere le coordinate al collegamento ipertestuale per una mappa immagine lato server in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldhyperlink/get_isimagemap/
---
## FieldHyperlink::get_IsImageMap method


Ottiene o imposta se aggiungere coordinate al hyperlink per una mappa immagine lato server.

```cpp
bool Aspose::Words::Fields::FieldHyperlink::get_IsImageMap()
```


## Esempi



Mostra come utilizzare i campi HYPERLINK per collegare documenti nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Quando facciamo clic su questo campo HYPERLINK in Microsoft Word,
// aprirà il documento collegato e poi posizionerà il cursore sul segnalibro specificato.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Quando facciamo clic su questo campo HYPERLINK in Microsoft Word,
// aprirà il documento collegato e scorrerà automaticamente verso il iframe specificato.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Vedi anche

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
