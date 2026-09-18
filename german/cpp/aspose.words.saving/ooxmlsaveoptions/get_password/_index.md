---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password method"
linktitle: "get_Password"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password method. Gibt ein Passwort zurück bzw. setzt es, um das Dokument mit dem ECMA376‑Standardverschlüsselungsalgorithmus in C++ zu verschlüsseln."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Liest/setzt ein Passwort, um das Dokument mit dem ECMA376-Standardverschlüsselungsalgorithmus zu verschlüsseln.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Hinweise


Um ein Dokument ohne Verschlüsselung zu speichern, sollte diese Eigenschaft **null** oder ein leerer String sein.

## Beispiele



Zeigt, wie man ein passwortverschlüsseltes Office Open XML‑Dokument erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// Wir können dieses Dokument nicht mit Microsoft Word oder
// Aspose.Words öffnen, ohne das korrekte Passwort anzugeben.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Öffnen Sie das verschlüsselte Dokument, indem Sie das korrekte Passwort in einem LoadOptions‑Objekt übergeben.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
