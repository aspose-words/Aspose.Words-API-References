---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeImporter class. Gör det möjligt att effektivt utföra upprepade import av noder från ett dokument till ett annat. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 44000
url: /sv/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Tillåter att effektivt utföra upprepad import av noder från ett dokument till ett annat. För att lära dig mer, besök dokumentationsartikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) i dokumentationen.

```cpp
class NodeImporter : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importerar en nod från ett dokument till ett annat. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Initierar en ny instans av klassen [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Initierar en ny instans av klassen [NodeImporter](./). |
| static [Type](./type/)() |  |
## Anmärkningar


Aspose.Words tillhandahåller funktionalitet för enkel kopiering och flyttning av fragment mellan Microsoft Word-dokument. Detta kallas "import av noder". Innan du kan infoga ett fragment från ett dokument till ett annat måste du "importera" det. Importering skapar en djup klon av den ursprungliga noden, redo att infogas i destinationsdokumentet.

Det enklaste sättet att importera en nod är att använda metoden [ImportNode()](../) som tillhandahålls av objektet [DocumentBase](../documentbase/).

När du däremot behöver importera noder från ett dokument till ett annat flera gånger är det bättre att använda klassen [NodeImporter](./). Klassen [NodeImporter](./) gör det möjligt att minimera antalet stilar och listor som skapas i destinationsdokumentet.

Att kopiera eller flytta fragment från ett Microsoft Word-dokument till ett annat medför ett antal tekniska utmaningar för Aspose.Words. I ett Word-dokument lagras stilar och listformatering centralt, separat från dokumentets text. Paragraferna och textkörningarna refererar bara till stilarna via interna unika identifierare.

Utmaningarna beror på att stilar och listor skiljer sig åt i olika dokument. Till exempel, för att kopiera ett stycke formaterat med stilen Rubrik 1 från ett dokument till ett annat, måste flera faktorer beaktas: avgöra om Rubrik 1‑stilen ska kopieras från källdokumentet till destinationsdokumentet, klona stycket, uppdatera det klonade stycket så att det refererar till rätt Rubrik 1‑stil i destinationsdokumentet. Om stilen måste kopieras bör alla stilar som den refererar till (baserat på stil och nästa stycke‑stil) analyseras och eventuellt också kopieras, och så vidare. Liknande problem uppstår vid kopiering av punktlistor eller numrerade stycken eftersom Microsoft Word lagrar listdefinitioner separat från texten.

Klassen [NodeImporter](./) fungerar som ett sammanhang som håller "översättningstabeller" under importen. Den översätter korrekt mellan stilar och listor i käll- och destinationsdokumenten.

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
