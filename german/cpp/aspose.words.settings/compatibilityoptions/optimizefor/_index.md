---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor Methode"
linktitle: "OptimizeFor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor Methode. Ermöglicht die Optimierung des Dokumentinhalts sowie des Standardverhaltens von Aspose.Words für bestimmte Versionen von MS Word. Verwenden Sie diese Methode, um zu verhindern, dass MS Word beim Laden des Dokuments die Registerkarte \"Kompatibilitätsmodus\" anzeigt. (Hinweis: Möglicherweise müssen Sie die Compliance‑Eigenschaft auf Iso29500_2008_Transitional oder höher setzen.) in C++."
type: docs
weight: 75000
url: /de/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


Ermöglicht die Optimierung des Dokumentinhalts sowie des Standardverhaltens von Aspose.Words für bestimmte Versionen von MS Word. Verwenden Sie diese Methode, um zu verhindern, dass MS Word beim Laden des Dokuments die Registerkarte "Kompatibilitätsmodus" anzeigt. (Hinweis: Möglicherweise müssen Sie die [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) Eigenschaft auf [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) oder höher setzen.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
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


Zeigt, wie der Textinhalt einer Textbox vertikal ausgerichtet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Top", um
// den Text in dieser Textbox mit der oberen Seite der Form auszurichten.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Middle", um
// den Text in dieser Textbox in der Mitte der Form auszurichten.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Bottom", um
// den Text in dieser Textbox an der Unterseite der Form auszurichten.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Die vertikale Ausrichtung von Text in Textboxen ist ab Microsoft Word 2007 verfügbar.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Siehe auch

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
