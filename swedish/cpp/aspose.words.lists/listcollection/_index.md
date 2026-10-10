---
title: "Aspose::Words::Lists::ListCollection klass"
linktitle: "ListCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListCollection-klass. Lagrar och hanterar formatering av punkt- och numrerade listor som används i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Lagrar och hanterar formatering av punkt- och numrerade listor som används i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Skapar en ny lista baserad på en fördefinierad mall och lägger till den i samlingen av listor i dokumentet. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Skapar en ny lista som refererar till en liststil och lägger till den i samlingen av listor i dokumentet. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Skapar en ny lista genom att kopiera den angivna listan och lägga till den i samlingen av listor i dokumentet. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Skapar en ny enkelnivålista baserad på den fördefinierade mallen och lägger till den i listsamlingen i dokumentet. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet numrerade och punktlistor i dokumentet. |
| [get_Document](./get_document/)() const | Hämtar ägardokumentet. |
| [GetEnumerator](./getenumerator/)() override | Hämtar enumeratorobjektet som kommer att iterera listor i dokumentet. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Hämtar en lista med ett listidentifierare. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar en lista efter index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Anmärkningar


En lista i ett Microsoft Word-dokument är en uppsättning listformaterings‑egenskaper. Formateringen av listorna lagras i [ListCollection](./)-samlingen separat från textparagraferna.

Du skapar inte objekt av den här klassen. Det finns alltid bara ett [ListCollection](./)-objekt per dokument och det är åtkomligt via egenskapen [Lists](../../aspose.words/documentbase/get_lists/).

För att skapa en ny lista baserad på en fördefinierad listmall eller baserad på en liststil, använd metoden [Add()](../).

För att skapa en ny lista med formatering identisk med en befintlig lista, använd metoden [AddCopy()](../).

För att göra ett stycke punktlistat eller numrerat, måste du tillämpa listformatering på ett stycke genom att tilldela ett [List](../list/)-objekt till [List](../listformat/get_list/)-egenskapen i [ListFormat](../listformat/).

För att ta bort listformatering från ett stycke, använd metoden [RemoveNumbers](../listformat/removenumbers/).

Om du vet lite om WordprocessingML, så kanske du vet att det definierar separata begrepp för "list" och "list definition". Detta motsvarar exakt hur listformatering lagras i ett Microsoft Word-dokument på låg nivå. [List](../list/)-definitionen är som ett "schema" och listan är som en instans av en listdefinition.

För att förenkla programmeringsmodellen döljer Aspose.Words skillnaden mellan lista och listdefinition på samma sätt som Microsoft Word döljer detta i sitt användargränssnitt. Detta låter dig fokusera mer på hur du vill att ditt dokument ska se ut, snarare än att bygga låg‑nivå‑objekt för att uppfylla kraven i Microsoft Word‑filformatet.

Det är inte möjligt att ta bort listor när de har skapats i den aktuella versionen av [Aspose.Words](../../aspose.words/). Detta liknar Microsoft Word där användaren inte har explicit kontroll över listdefinitioner.

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


Visar hur man startar om numrering i en lista genom att kopiera en lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Applicera vår lista på några stycken.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Vi kan lägga till en kopia av en befintlig lista till dokumentets listsamling
// för att skapa en liknande lista utan att ändra originalet.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Applicera den andra listan på nya stycken.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Se även

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
