---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Checked Methode"
linktitle: "get_Checked"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Checked Methode. Ruft den aktuellen Zustand des Checkbox‑SDT ab bzw. legt ihn fest. Der Standardwert für diese Eigenschaft ist false in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Liest/legt den aktuellen Zustand der Checkbox **SDT** fest. Der Standardwert für diese Eigenschaft ist **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Hinweise


Der Zugriff auf diese Eigenschaft funktioniert nur für [Checkbox](../../sdttype/) SDT-Typen.

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
