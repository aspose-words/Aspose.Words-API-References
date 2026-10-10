---
title: "Aspose::Words::Lists::ListTemplate-enum"
linktitle: "ListTemplate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListTemplate-enum. Anger ett av de fördefinierade listformaten som finns i Microsoft Word i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.lists/listtemplate/
---
## ListTemplate enum


Anger ett av de fördefinierade listformaten som finns i Microsoft Word.

```cpp
enum class ListTemplate
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| BulletDefault | 0 | Standard punktlista med 9 nivåer. Punkttecknet på den första nivån är en skiva, på den andra nivån är en cirkel, på den tredje nivån är en fyrkant. Därefter upprepas formateringen för de återstående nivåerna. Varje nivå är indenterad åt höger med 0.25\" relativt föregående nivå. Motsvarar den 1:a punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| BulletDisk | n/a | Samma som [BulletDefault](./). Motsvarar den 1:a punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| BulletCircle | n/a | Punkttecknet på den första nivån är en cirkel. De återstående nivåerna är samma som i [BulletDefault](./). Motsvarar den 2:a punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| BulletSquare | n/a | Punkttecknet på den första nivån är en fyrkant. De återstående nivåerna är samma som i [BulletDefault](./). Motsvarar den 3:e punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| BulletDiamonds | n/a | Punkttecknet på den första nivån är ett 4-diamant Wingding-tecken. De återstående nivåerna är samma som i [BulletDefault](./). Motsvarar den 5:e punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| BulletArrowHead | n/a | Punkttecknet på den första nivån är ett pilspets Wingding-tecken. De återstående nivåerna är samma som i [BulletDefault](./). Motsvarar den 6:e punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| BulletTick | n/a | Punkttecknet på den första nivån är ett bockmarkering Wingding-tecken. De återstående nivåerna är samma som i [BulletDefault](./). Motsvarar den 7:e punktlistmall i dialogrutan Punkter och numrering i Microsoft Word. |
| NumberDefault | n/a | Standardnumrerad lista med 9 nivåer. Arabisk numrering (1., 2., 3., ...) för den första nivån, gemener bokstavsnumrering (a., b., c., ...) för den andra nivån, gemener romersk numrering (i., ii., iii., ...) för den tredje nivån. Därefter upprepas formateringen för de återstående nivåerna. Varje nivå är indenterad åt höger med 0,25\" i förhållande till föregående nivå. Motsvarar den 1:a numrerade listmall i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberArabicDot | n/a | Samma som [NumberDefault](./). Motsvarar den 1:a numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberArabicParenthesis | n/a | Numret för den första nivån är \"1)\". De återstående nivåerna är samma som i [NumberDefault](./). Motsvarar den 2:a numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberUppercaseRomanDot | n/a | Numret för den första nivån är \"I.\". De återstående nivåerna är samma som i [NumberDefault](./). Motsvarar den 3:e numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberUppercaseLetterDot | n/a | Numret för den första nivån är \"A.\". De återstående nivåerna är samma som i [NumberDefault](./). Motsvarar den 4:e numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberLowercaseLetterParenthesis | n/a | Numret för den första nivån är \"a)\". De återstående nivåerna är samma som i [NumberDefault](./). Motsvarar den 5:e numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberLowercaseLetterDot | n/a | Numret för den första nivån är \"a.\". De återstående nivåerna är samma som i [NumberDefault](./). Motsvarar den 6:e numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| NumberLowercaseRomanDot | n/a | Numret för den första nivån är \"i.\". De återstående nivåerna är samma som i [NumberDefault](./). Motsvarar den 7:e numrerade listmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineNumbers | n/a | En dispositionslista med nivåer numrerade \"1), a), i), (1), (a), (i), 1., a., i.\". Motsvarar den 1:a dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineLegal | n/a | En dispositionslista med nivåer numrerade \"1., 1.1., 1.1.1, ...\". Motsvarar den 2:a dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineBullets | n/a | En dispositionslista med olika punkter för olika nivåer. Motsvarar den 3:e dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineHeadingsArticleSection | n/a | En dispositionslista med nivåer kopplade till rubrikformat. Motsvarar den 4:e dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineHeadingsLegal | n/a | En dispositionslista med nivåer kopplade till rubrikformat. Motsvarar den 5:e dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineHeadingsNumbers | n/a | En dispositionslista med nivåer kopplade till rubrikformat. Motsvarar den 6:e dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |
| OutlineHeadingsChapter | n/a | En dispositionslista med nivåer kopplade till rubrikformat. Motsvarar den 7:e dispositionslistmallen i dialogrutan Punktlistor och numrering i Microsoft Word. |

## Anmärkningar


Ett listmallvärde används som parameter i metoden [Add()](../listcollection/add/).

Aspose.Words-listmallar motsvarar de 21 listmallarna som finns i dialogrutan Punkter och numrering i Microsoft Word 2003.

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
