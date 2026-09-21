---
title: "Aspose::Words::Fields::FieldHyperlink::get_Address metod"
linktitle: "get_Address"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldHyperlink::get_Address metod. Hämtar eller anger en plats dit denna hyperlänk hoppar i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldhyperlink/get_address/
---
## FieldHyperlink::get_Address method


Hämtar eller anger en plats dit den här hyperlänken hoppar.

```cpp
System::String Aspose::Words::Fields::FieldHyperlink::get_Address()
```


## Exempel



Visar hur man använder HYPERLINK-fält för att länka till dokument i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// När vi klickar på detta HYPERLINK-fält i Microsoft Word,
// den kommer att öppna det länkade dokumentet och sedan placera markören vid det angivna bokmärket.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// När vi klickar på detta HYPERLINK-fält i Microsoft Word,
// den kommer att öppna det länkade dokumentet och automatiskt scrolla ner till den angivna iframe.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Se även

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
