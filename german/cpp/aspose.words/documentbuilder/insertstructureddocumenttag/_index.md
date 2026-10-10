---
title: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method"
linktitle: "InsertStructuredDocumentTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method. Fügt ein StructuredDocumentTag in das Dokument in C++ ein."
type: docs
weight: 46500
url: /de/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Fügt ein [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

Der [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) Knoten, der gerade eingefügt wurde.

## Beispiele



Zeigt, wie man einfach ein strukturiertes Dokument-Tag einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Hinweis: Es dürfen nur die folgenden StructuredDocumentTag‑Typen eingefügt werden:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Die Markup‑Ebene des eingefügten StructuredDocumentTag wird automatisch erkannt und hängt von der Position ab, an der es eingefügt wird.
// Das hinzugefügte StructuredDocumentTag erbt Absatz‑ und Schriftformatierung von der Cursor‑Position.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
