---
title: Aspose::Words::Fields::FieldPrint::set_PostScriptGroup method
linktitle: set_PostScriptGroup
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldPrint::set_PostScriptGroup method. Sets the drawing rectangle that the PostScript instructions operate on in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.fields/fieldprint/set_postscriptgroup/
---
## FieldPrint::set_PostScriptGroup method


Sets the drawing rectangle that the PostScript instructions operate on.

```cpp
void Aspose::Words::Fields::FieldPrint::set_PostScriptGroup(const System::String & value)
```

## Examples


Shows to insert a PRINT field.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// The PRINT field can send instructions to the printer.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(FieldType::FieldPrint, true));

// Set the area for the printer to perform instructions over.
// In this case, it will be the paragraph that contains our PRINT field.
field->set_PostScriptGroup(u"para");

// When we use a printer that supports PostScript to print our document,
// this command will turn the entire area that we specified in "field.PostScriptGroup" white.
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```
## See Also

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
