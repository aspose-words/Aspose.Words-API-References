---
title: Aspose::Words::Fields::FieldPrint::get_PrinterInstructions method
linktitle: get_PrinterInstructions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldPrint::get_PrinterInstructions method. Gets or sets the printer-specific control code characters or PostScript instructions in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fieldprint/get_printerinstructions/
---
## FieldPrint::get_PrinterInstructions method


Gets or sets the printer-specific control code characters or PostScript instructions.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PrinterInstructions()
```


## Examples



Shows to insert a PRINT field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// The PRINT field can send instructions to the printer.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

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
