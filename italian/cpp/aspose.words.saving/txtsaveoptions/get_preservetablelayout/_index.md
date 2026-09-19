---
title: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout metodo"
linktitle: "get_PreserveTableLayout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout. Specifica se il programma deve tentare di preservare la disposizione delle tabelle durante il salvataggio nel formato di testo semplice. Il valore predefinito è false in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Specifica se il programma deve tentare di preservare la disposizione delle tabelle durante il salvataggio in formato testo semplice. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Esempi



Mostra come preservare la disposizione delle tabelle durante la conversione in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Imposta la proprietà "PreserveTableLayout" su "true" per applicare riempimento di spazi bianchi al contenuto
// del documento di testo semplice di output per preservare il più possibile la disposizione della tabella.
// Imposta la proprietà "PreserveTableLayout" su "false" per salvare tutti i contenuti delle tabelle
// come un corpo continuo di testo, con una sola nuova riga per ogni riga.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## Vedi anche

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
