---
title: "Aspose::Words::Fields::FieldRD::get_IsPathRelative-Methode"
linktitle: "get_IsPathRelative"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldRD::get_IsPathRelative-Methode. Ruft ab oder legt fest, ob der Pfad relativ zum aktuellen Dokument in C++ ist."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldrd/get_ispathrelative/
---
## FieldRD::get_IsPathRelative method


Ruft ab, ob der Pfad relativ zum aktuellen Dokument ist, oder legt dies fest.

```cpp
bool Aspose::Words::Fields::FieldRD::get_IsPathRelative()
```


## Beispiele



Zeigt, wie das RD-Feld verwendet wird, um Einträge im Inhaltsverzeichnis aus Überschriften in anderen Dokumenten zu erstellen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie einen DocumentBuilder, um ein Inhaltsverzeichnis einzufügen,
// und fügen Sie dann einen Eintrag für das Inhaltsverzeichnis auf der folgenden Seite hinzu.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Fügen Sie ein RD-Feld ein, das in seiner FileName‑Eigenschaft auf ein anderes lokales Dateisystemdokument verweist.
// Das Inhaltsverzeichnis akzeptiert nun auch alle Überschriften aus dem referenzierten Dokument als Einträge für seine Tabelle.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// Erstellen Sie das Dokument, auf das das RD-Feld verweist, und fügen Sie eine Überschrift ein.
// Diese Überschrift wird als Eintrag im TOC‑Feld unseres ersten Dokuments angezeigt.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## Siehe auch

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
