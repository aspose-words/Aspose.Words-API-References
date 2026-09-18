---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol Methode"
linktitle: "SetCheckedSymbol"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol Methode. Legt das Symbol fest, das verwendet wird, um den aktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements in C++ darzustellen."
type: docs
weight: 58000
url: /de/cpp/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag::SetCheckedSymbol method


Legt das Symbol fest, das verwendet wird, um den aktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements darzustellen.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| characterCode | int32_t | Der Zeichencode für das angegebene Symbol. |
| fontName | const System::String\& | Der Name der Schriftart, die das Symbol enthält. |
## Hinweise


Der Zugriff auf diese Methode funktioniert nur für [Checkbox](../../sdttype/) SDT-Typen.

Für alle anderen SDT‑Typen wird eine Ausnahme auftreten.

## Beispiele



Zeigen Sie, wie man ein strukturiertes Dokument-Tag in Form einer Checkbox erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Wir können die Symbole festlegen, die den aktivierten/deaktivierten Zustand einer Checkbox-Inhaltssteuerelement darstellen.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
