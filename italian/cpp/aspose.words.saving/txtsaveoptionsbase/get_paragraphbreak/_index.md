---
title: "Metodo Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak"
linktitle: "get_ParagraphBreak"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak. Specifica la stringa da utilizzare come interruzione di paragrafo durante l'esportazione in formati di testo in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/txtsaveoptionsbase/get_paragraphbreak/
---
## TxtSaveOptionsBase::get_ParagraphBreak method


Specifica la stringa da utilizzare come interruzione di paragrafo durante l'esportazione in formati di testo.

```cpp
System::String Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak() const
```

## Note


Il valore predefinito è [CrLf](../../../aspose.words/controlchar/crlf/).

## Esempi



Mostra come salvare un documento .txt con un'interruzione di paragrafo personalizzata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Imposta "ParagraphBreak" a un valore personalizzato che desideriamo inserire alla fine di ogni paragrafo.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Vedi anche

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
