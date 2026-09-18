---
title: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions-Konstruktor"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions-Konstruktor. Initialisiert eine neue Instanz dieser Klasse mit Standardwerten in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Beispiele



Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Wenn der Wert true ist, berücksichtigen wir VML-Code beim Parsen des geladenen Dokuments.
loadOptions->set_SupportVml(supportVml);

// Dieses Dokument enthält ein JPEG-Bild innerhalb von "<!--[if gte vml 1]>"-Tags,
// und ein anderes PNG-Bild innerhalb von "<![if !vml]>"-Tags.
// Wenn wir das Flag "SupportVml" auf "true" setzen, lädt Aspose.Words das JPEG.
// Wenn wir dieses Flag auf "false" setzen, lädt Aspose.Words nur das PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Siehe auch

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Ein Shortcut, um eine neue Instanz dieser Klasse mit auf die angegebenen Werte gesetzten Eigenschaften zu initialisieren.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


Ein Shortcut, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | const System::String\& | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann **null** oder eine leere Zeichenfolge sein. |

## Beispiele



Zeigt, wie man ein Html-Dokument verschlüsselt und anschließend mit einem Passwort öffnet.
```cpp
// Erstellt und signiert ein verschlüsseltes HTML-Dokument aus einer verschlüsselten .docx-Datei.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Um dieses Dokument zu laden und zu lesen, müssen wir seine Entschlüsselung übergeben
// Passwort mithilfe eines HtmlLoadOptions-Objekts.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## Siehe auch

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
