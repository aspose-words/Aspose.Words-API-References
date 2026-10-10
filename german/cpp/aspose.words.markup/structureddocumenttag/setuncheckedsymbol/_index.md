---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol Methode"
linktitle: "SetUncheckedSymbol"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol Methode. Legt das Symbol fest, das den nicht aktivierten Zustand einer Kontrollkästchen-Inhaltssteuerelement in C++ darstellt."
type: docs
weight: 59000
url: /de/cpp/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag::SetUncheckedSymbol method


Legt das Symbol fest, das verwendet wird, um den deaktivierten Zustand eines Kontrollkästchen-Inhaltssteuerelements darzustellen.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol(int32_t characterCode, const System::String &fontName)
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
