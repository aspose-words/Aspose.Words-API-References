---
title: "Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag-Konstruktor"
linktitle: "StructuredDocumentTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag-Konstruktor. Initialisiert eine neue Instanz der Structured‑Document‑Tag‑Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Initialisiert eine neue Instanz der Klasse **Structured document tag**.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
| Typ | Aspose::Words::Markup::SdtType | Typ des SDT‑Knotens. |
| Ebene | Aspose::Words::Markup::MarkupLevel | Ebene des SDT‑Knotens im Dokument. |
## Hinweise


Die folgenden SDT‑Typen können erstellt werden:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
