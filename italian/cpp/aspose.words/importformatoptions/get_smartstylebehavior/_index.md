---
title: "Metodo Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior"
linktitle: "get_SmartStyleBehavior"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior. Ottiene o imposta un valore booleano che specifica come gli stili saranno importati quando hanno lo stesso nome nei documenti di origine e destinazione. Il valore predefinito è false in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Ottiene o imposta un valore booleano che specifica come verranno importati gli stili quando hanno lo stesso nome nei documenti di origine e destinazione. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Note


Quando questa opzione è **enabled**, lo stile di origine verrà espanso in attributi diretti all'interno del documento di destinazione, se viene utilizzata la modalità di importazione [KeepSourceFormatting](../../importformatmode/).

Quando questa opzione è **disabled**, lo stile di origine verrà espanso solo se è numerato. Gli attributi di destinazione esistenti non saranno sovrascritti, incluse le liste.

## Esempi



Mostra come risolvere gli stili duplicati durante l'inserimento dei documenti.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clona il documento e modifica lo stile "MyStyle" del clone, in modo che abbia un colore diverso rispetto a quello originale.
// Se inseriamo il clone nel documento originale, i due stili con lo stesso nome provocheranno un conflitto.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Quando abilitiamo SmartStyleBehavior e utilizziamo la modalità di importazione KeepSourceFormatting,
// Aspose.Words risolverà i conflitti di stile convertendo gli stili del documento di origine.
// con gli stessi nomi degli stili di destinazione in attributi di paragrafo diretti.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
