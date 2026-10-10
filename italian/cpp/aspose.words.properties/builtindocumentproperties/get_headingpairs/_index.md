---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs metodo"
linktitle: "get_HeadingPairs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs metodo. Specifica le intestazioni del documento e i loro nomi in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Specifica le intestazioni del documento e i loro nomi.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Note


Ogni coppia di intestazioni occupa due elementi in questo array.

Il primo elemento della coppia è una **String** e specifica il nome dell'intestazione. Il secondo elemento della coppia è un **Int32** e specifica il conteggio delle parti del documento per questa intestazione nella proprietà [TitlesOfParts](../get_titlesofparts/).

La somma totale dei conteggi per tutte le coppie di intestazioni in questa proprietà deve essere uguale al numero di elementi nella proprietà [TitlesOfParts](../get_titlesofparts/).

Aspose.Words non aggiorna questa proprietà.

## Esempi



Mostra la relazione tra le proprietà \"HeadingPairs\" e \"TitlesOfParts\".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Possiamo trovare i valori combinati di queste collezioni tramite
// "File" -> "Proprietà" -> "Proprietà avanzate" -> "Contenuto" scheda.
// La proprietà HeadingPairs è una collezione di coppie <string, int> che
// determina quante parti del documento copre un'intestazione.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// La proprietà TitlesOfParts contiene i nomi delle parti che appartengono alle intestazioni precedenti.
System::ArrayPtr<System::String> titlesOfParts = doc->get_BuiltInDocumentProperties()->get_TitlesOfParts();

int32_t headingPairsIndex = 0;
int32_t titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs->get_Length())
{
    std::cout << System::String::Format(u"Parts for {0}:", headingPairs[headingPairsIndex++]) << std::endl;
    int32_t partsCount = System::Convert::ToInt32(headingPairs[headingPairsIndex++]);

    for (int32_t i = 0; i < partsCount; i++)
    {
        std::cout << System::String::Format(u"\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]) << std::endl;
    }
}
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
