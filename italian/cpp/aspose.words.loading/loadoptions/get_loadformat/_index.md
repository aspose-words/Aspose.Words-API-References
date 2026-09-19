---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method"
linktitle: "get_LoadFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method. Specifica il formato del documento da caricare. Il valore predefinito è Auto in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Specifica il formato del documento da caricare. Il valore predefinito è [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Note


Si consiglia di specificare il valore [Auto](../../../aspose.words/loadformat/) e lasciare che Aspose.Words rilevi automaticamente il formato del file. Se conosci il formato del documento che stai per caricare, puoi specificarlo esplicitamente e questo ridurrà leggermente il tempo di caricamento eliminando l'overhead associato al rilevamento automatico del formato. Se specifichi un formato di caricamento esplicito e dovesse risultare errato, verrà invocata la rilevazione automatica e verrà effettuato un secondo tentativo di caricamento del file.

## Esempi



Mostra come specificare un URI di base quando si apre un documento html.
```cpp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata tramite un URI relativo
// mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
// Possiamo fornire un URI di base usando un oggetto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Mentre l'immagine era interrotta nell'html di input, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Questo documento di output visualizzerà l'immagine che mancava.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Vedi anche

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
