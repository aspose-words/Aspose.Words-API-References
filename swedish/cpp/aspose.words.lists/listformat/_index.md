---
title: "Aspose::Words::Lists::ListFormat klass"
linktitle: "ListFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListFormat klass. Tillåter att kontrollera vilken listformatering som tillämpas på ett stycke. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Tillåter att styra vilken listformatering som tillämpas på ett stycke. För att lära dig mer, besök dokumentationsartikeln [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Startar en ny standardpunktlista och tillämpar den på stycket. |
| [ApplyNumberDefault](./applynumberdefault/)() | Startar en ny standardnumrerad lista och tillämpar den på stycket. |
| [get_IsListItem](./get_islistitem/)() | Sant när stycket har punkt- eller numrerad formatering tillämpad på det. |
| [get_List](./get_list/)() | Hämtar eller anger listan som detta stycke är medlem i. |
| [get_ListLevel](./get_listlevel/)() | Returnerar listnivåns formatering plus eventuella formateringsöverskrivningar som tillämpas på det aktuella stycket. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Hämtar eller anger listnivåns nummer (0 till 8) för stycket. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Ökar listnivån för det aktuella stycket med en nivå. |
| [ListOutdent](./listoutdent/)() | Minskar listnivån för det aktuella stycket med en nivå. |
| [RemoveNumbers](./removenumbers/)() | Tar bort siffror eller punkter från det aktuella stycket och sätter listnivån till noll. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Sättare för [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Sättare för [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Anmärkningar


Ett stycke i ett Microsoft Word-dokument kan vara punktlistat eller numrerat. När ett stycke är punktlistat eller numrerat sägs det att listformatering har tillämpats på stycket.

Du skapar inte objekt av klassen [ListFormat](./) direkt. Du får åtkomst till [ListFormat](./) som en egenskap hos ett annat objekt som kan ha listformatering associerad med sig. För närvarande är objekten som kan ha listformatering: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) och [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

Listformateringen själv lagras i ett [List](../list/) objekt som lagras separat från styckena. Listobjekten lagras i en [ListCollection](../listcollection/) samling. Det finns en enda [ListCollection](../listcollection/) samling per [Document](../../aspose.words/document/).

Styckena tillhör inte fysiskt en lista. Styckena refererar bara till ett specifikt listobjekt via egenskapen [List](./get_list/) och en specifik nivå i listan via egenskapen [ListLevelNumber](./get_listlevelnumber/). Genom att ange dessa två egenskaper styr du vilka punkter och numrering som tillämpas på ett stycke.

## Exempel



Visar hur man arbetar med listnivåer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Nedan finns två typer av listor som vi kan skapa med en dokumentbyggare.
// 1 -  En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Genom att sätta egenskapen "ListLevelNumber" kan vi öka listnivån
// för att påbörja en självständig underlista vid det aktuella listobjektet.
// Microsoft Word-listmallen som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
// Djupare listnivåer använder bokstäver och gemena romerska siffror.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  En punktlista:
// Denna lista kommer att applicera ett indrag och en punktsymbol ("•") före varje stycke.
// Djupare nivåer i denna lista kommer att använda olika symboler, såsom "■" och "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Vi kan inaktivera listformatering så att inga efterföljande stycken formateras som listor genom att avaktivera flaggan "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```

## Se även

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
