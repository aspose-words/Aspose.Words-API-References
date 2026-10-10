---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions Konstruktor"
linktitle: "LoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions Konstruktor. Initialisiert eine neue Instanz dieser Klasse mit Standardwerten in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Beispiele



Zeigt, wie man ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI öffnet.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Übergeben Sie beim Laden die URI des Basisordners
    // damit alle Bilder mit relativen URIs im HTML-Dokument gefunden werden können.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Überprüfen Sie, dass die erste Form des Dokuments ein gültiges Bild enthält.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Ein Shortcut, um eine neue Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften zu initialisieren.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | Das Format des zu ladenden Dokuments. |
| password | const System::String\& | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder eine leere Zeichenfolge sein. |
| baseUri | const System::String\& | Die Zeichenfolge, die verwendet wird, um relative URIs in absolute umzuwandeln. Kann **null** oder eine leere Zeichenfolge sein. |

## Beispiele



Zeigt, wie man beim Öffnen eines HTML-Dokuments eine Basis-URI angibt.
```cpp
// Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das über eine relative URI verlinkt ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir die relative URI in eine absolute URI auflösen.
// Wir können eine Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Obwohl das Bild im Eingabe-.html beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Siehe auch

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


Ein Shortcut, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | const System::String\& | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder eine leere Zeichenfolge sein. |

## Beispiele



Zeigt, wie man ein verschlüsseltes Microsoft Word-Dokument lädt.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words wirft eine Ausnahme, wenn wir versuchen, ein verschlüsseltes Dokument ohne dessen Passwort zu öffnen.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Beim Laden eines solchen Dokuments wird das Passwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 -  Laden Sie das Dokument vom lokalen Dateisystem über den Dateinamen:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Laden Sie das Dokument aus einem Stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
