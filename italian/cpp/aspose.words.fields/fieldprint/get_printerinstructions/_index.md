---
title: "Metodo Aspose::Words::Fields::FieldPrint::get_PrinterInstructions"
linktitle: "get_PrinterInstructions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldPrint::get_PrinterInstructions. Ottiene o imposta i caratteri di codice di controllo specifici della stampante o le istruzioni PostScript in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldprint/get_printerinstructions/
---
## FieldPrint::get_PrinterInstructions method


Ottiene o imposta i caratteri di codice di controllo specifici della stampante o le istruzioni PostScript.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PrinterInstructions()
```


## Esempi



Mostra come inserire un campo PRINT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// Il campo PRINT può inviare istruzioni alla stampante.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Imposta l'area su cui la stampante deve eseguire le istruzioni.
// In questo caso, sarà il paragrafo che contiene il nostro campo PRINT.
field->set_PostScriptGroup(u"para");

// Quando utilizziamo una stampante che supporta PostScript per stampare il nostro documento,
// questo comando renderà bianca l'intera area che abbiamo specificato in "field.PostScriptGroup".
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## Vedi anche

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
