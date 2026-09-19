---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method"
linktitle: "get_AddBidiMarks"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method. Specifica se aggiungere segni bidirezionali prima di ogni sequenza BiDi durante l'esportazione in formato testo semplice. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Specifica se aggiungere segni bidirezionali prima di ogni sequenza BiDi durante l'esportazione in formato testo semplice. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Esempi



Mostra come inserire il carattere Unicode 'RIGHT-TO-LEFT MARK' (U+200F) prima di ogni [Run](../../../aspose.words/run/) bidirezionale nel testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Imposta la proprietà "AddBidiMarks" su "true" per aggiungere segni prima delle sequenze
// con testo da destra a sinistra per indicare tale situazione.
// Imposta la proprietà "AddBidiMarks" su "false" per scrivere tutto da sinistra a destra
// e le sequenze da destra a sinistra allo stesso modo, senza nulla per indicare quale sia quale.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## Vedi anche

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
