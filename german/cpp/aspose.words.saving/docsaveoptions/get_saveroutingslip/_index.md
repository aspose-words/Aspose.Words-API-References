---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip Methode"
linktitle: "get_SaveRoutingSlip"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip Methode. Wenn false, werden RoutingSlip-Daten nicht im Ausgabedokument gespeichert. Der Standardwert ist true in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.saving/docsaveoptions/get_saveroutingslip/
---
## DocSaveOptions::get_SaveRoutingSlip method


Wenn **false**, werden RoutingSlip‑Daten nicht im Ausgabedokument gespeichert. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip() const
```


## Beispiele



Zeigt, wie man Speicheroptionen für ältere Microsoft‑Word‑Formate festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Legen Sie ein Passwort fest, das das Laden des Dokuments durch Microsoft Word oder Aspose.Words schützt.
// Beachten Sie, dass dies den Inhalt des Dokuments in keiner Weise verschlüsselt.
options->set_Password(u"MyPassword");

// Wenn das Dokument einen Routing‑Slip enthält, können wir ihn beim Speichern erhalten, indem wir dieses Flag auf true setzen.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// Um das Dokument laden zu können,
// müssen wir das Passwort, das wir im DocSaveOptions‑Objekt angegeben haben, in einem LoadOptions‑Objekt anwenden.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
