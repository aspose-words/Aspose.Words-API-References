---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method"
linktitle: "get_SimplifyListLabels"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method. Specifica se il programma deve semplificare le etichette delle liste nel caso in cui la formattazione complessa delle etichette non sia adeguatamente rappresentata in testo semplice. Se impostato su true, le etichette delle liste numerate vengono scritte in formato numerico semplice e le etichette delle liste puntate come semplici caratteri ASCII. Il valore predefinito è false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Specifica se il programma deve semplificare le etichette degli elenchi nel caso in cui una formattazione complessa delle etichette non sia adeguatamente rappresentata in testo semplice. Se impostato su **true**, le etichette degli elenchi numerati vengono scritte in formato numerico semplice e le etichette degli elenchi puntati come semplici caratteri ASCII. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Esempi



Mostra come modificare l'aspetto delle liste quando si salva un documento in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea una lista puntata con cinque livelli di rientro.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Imposta la proprietà "SimplifyListLabels" su "true" per convertire alcune liste
// i simboli in caratteri ASCII più semplici, come '*', 'o', '+', '>', ecc.
// Imposta la proprietà "SimplifyListLabels" su "false" per preservare il maggior numero possibile di simboli originali delle liste.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## Vedi anche

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
