---
title: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions Konstruktor"
linktitle: "OoxmlSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions Konstruktor. Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im Docx‑Format in C++ zu speichern."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Docx](../../../aspose.words/saveformat/) Format zu speichern.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
```


## Beispiele



Zeigt, wie man eine OOXML‑Compliance‑Spezifikation für ein gespeichertes Dokument festlegt, an die es sich halten muss.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn wir Kompatibilitätsoptionen so konfigurieren, dass sie mit Microsoft Word 2003 konform sind,
// Das Einfügen eines Bildes definiert seine Form mithilfe von VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Der "ISO/IEC 29500:2008" OOXML‑Standard unterstützt keine VML‑Formen.
// Wenn wir die "Compliance"‑Eigenschaft des SaveOptions‑Objekts auf "OoxmlCompliance.Iso29500_2008_Strict" setzen,
// muss jedes Dokument, das wir beim Übergeben dieses Objekts speichern, diesem Standard folgen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Unser gespeichertes Dokument definiert die Form mithilfe von DML, um dem "ISO/IEC 29500:2008" OOXML‑Standard zu entsprechen.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## Siehe auch

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) oder [FlatOpc](../../../aspose.words/saveformat/) Format zu speichern.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Kann [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) oder [FlatOpc](../../../aspose.words/saveformat/) sein. |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
