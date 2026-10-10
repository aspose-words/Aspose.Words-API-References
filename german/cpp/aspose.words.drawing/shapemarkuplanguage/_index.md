---
title: "Aspose::Words::Drawing::ShapeMarkupLanguage Aufzählung"
linktitle: "ShapeMarkupLanguage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeMarkupLanguage Aufzählung. Gibt die für die Form in C++ verwendete Auszeichnungssprache an."
type: docs
weight: 37000
url: /de/cpp/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enum


Gibt die [Markup](../../aspose.words.markup/) Sprache an, die für die Form verwendet wird.

```cpp
enum class ShapeMarkupLanguage : uint8_t
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Dml | 0 | [Drawing](../)[Markup](../../aspose.words.markup/) Sprache wird verwendet, um die Form zu definieren. |
| Vml | 1 | Vektor [Markup](../../aspose.words.markup/) Sprache wird verwendet, um die Form zu definieren. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
