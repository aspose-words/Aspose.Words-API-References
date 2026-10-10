---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase metodo"
linktitle: "get_HyperlinkBase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase metodo. Specifica la stringa base utilizzata per valutare gli hyperlink relativi in questo documento in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Specifica la stringa di base utilizzata per valutare i collegamenti ipertestuali relativi in questo documento.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Note


Aspose.Words non utilizza questa proprietà.

## Esempi



Mostra come memorizzare la parte base di un hyperlink nelle proprietà del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un hyperlink relativo a un documento nel file system locale denominato "Document.docx".
// Facendo clic sul collegamento in Microsoft Word si aprirà il documento designato, se è disponibile.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Questo collegamento è relativo. Se non c'è "Document.docx" nella stessa cartella
// come il documento che contiene questo collegamento, il collegamento sarà interrotto.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Il documento a cui stiamo cercando di collegarci si trova in una directory diversa da quella in cui prevediamo di salvare il documento.
// Potremmo correggere i collegamenti in questo modo inserendo un nome file assoluto in ciascuno.
// In alternativa, potremmo fornire un collegamento base che ogni hyperlink con un nome file relativo
// verrà anteposto al suo collegamento quando ci clicchiamo sopra.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
