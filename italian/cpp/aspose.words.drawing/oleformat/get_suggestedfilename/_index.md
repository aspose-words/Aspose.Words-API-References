---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName metodo"
linktitle: "get_SuggestedFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName metodo. Ottiene il nome file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Ottiene il nome file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Esempi



Mostra come ottenere il nome file suggerito di un oggetto OLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// Gli oggetti OLE possono fornire un nome file e un'estensione suggeriti,
// che possiamo utilizzare quando salviamo il contenuto dell'oggetto in un file nel file system locale.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## Vedi anche

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
