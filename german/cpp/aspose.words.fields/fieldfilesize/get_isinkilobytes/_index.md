---
title: "Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes Methode"
linktitle: "get_IsInKilobytes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes Methode. Gibt an oder legt fest, ob die Dateigröße in Kilobyte angezeigt werden soll, in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldfilesize/get_isinkilobytes/
---
## FieldFileSize::get_IsInKilobytes method


Ermittelt oder legt fest, ob die Dateigröße in Kilobyte angezeigt wird.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes()
```


## Beispiele



Zeigt, wie die Dateigröße eines Dokuments mit einem FILESIZE‑Feld angezeigt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Nachfolgend sind drei verschiedene Maßeinheiten aufgeführt
// mit denen FILESIZE‑Felder die Dateigröße des Dokuments anzeigen können.
// 1 -  Bytes:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobytes:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabytes:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// Um die Werte dieser Felder beim Bearbeiten in Microsoft Word zu aktualisieren,
// müssen wir zuerst die Änderungen speichern und dann diese Felder manuell aktualisieren.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## Siehe auch

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
