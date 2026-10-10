---
title: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate Methode"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate method. Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung in C++ vollständig unterstützt wird oder nicht."
type: docs
weight: 15000
url: /de/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Liest oder setzt den Wert, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Hinweise


Wenn diese Eigenschaft auf **true** gesetzt ist, werden zusätzliche Schritte ausgeführt, um ein mit Rechts-nach-Links-Sprachen (z. B. Arabisch oder Hebräisch) kompatibles Feldergebnis während der Aktualisierung zu erzeugen.

Wenn diese Eigenschaft auf **false** gesetzt ist und eine Rechts-nach-Links-Sprache verwendet wird, ist die Korrektheit des Feldergebnisses nach seiner Aktualisierung nicht garantiert.

Der Standardwert ist **false**.

## Beispiele



Zeigt, wie man [FieldOptions](../) verwendet, um sicherzustellen, dass die Feldaktualisierung bidirektionalen Text vollständig unterstützt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Stellen Sie sicher, dass jede Feldoperation, die Rechts-nach-Links-Text beinhaltet, wie erwartet ausgeführt wird.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Verwenden Sie einen Document Builder, um ein Feld einzufügen, das Rechts-nach-Links-Text enthält.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## Siehe auch

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
