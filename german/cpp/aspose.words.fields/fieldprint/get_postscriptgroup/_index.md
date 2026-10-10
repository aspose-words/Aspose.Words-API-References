---
title: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup Methode"
linktitle: "get_PostScriptGroup"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup Methode. Ruft das Zeichenrechteck ab oder legt es fest, auf das die PostScript-Anweisungen in C++ angewendet werden."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


Liest oder setzt das Zeichenrechteck, auf dem die PostScript-Anweisungen ausgeführt werden.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
```


## Beispiele



Zeigt das Einfügen eines PRINT-Feldes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// Das PRINT-Feld kann Anweisungen an den Drucker senden.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Legen Sie den Bereich fest, in dem der Drucker Anweisungen ausführt.
// In diesem Fall ist es der Absatz, der unser PRINT-Feld enthält.
field->set_PostScriptGroup(u"para");

// Wenn wir einen Drucker verwenden, der PostScript unterstützt, um unser Dokument zu drucken,
// wird dieser Befehl den gesamten Bereich, den wir in "field.PostScriptGroup" angegeben haben, weiß färben.
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## Siehe auch

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
