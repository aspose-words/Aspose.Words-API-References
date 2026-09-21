---
title: "Aspose::Words::MailMerging::MailMerge::Execute metod"
linktitle: "Utför"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::MailMerge::Execute method. Utför en kopplad utskriftsoperation för en enda post i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Utför en kopplingsoperation för en enskild post.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Array med namn på sammanslagningsfält. Fältnamn är inte skiftlägeskänsliga. Om ett fältnamn som inte finns i dokumentet påträffas, ignoreras det. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Array med värden som ska infogas i sammanslagningsfälten. Antalet element i denna array måste vara samma som antalet element i *fieldNames*. |
## Anmärkningar


Använd den här metoden för att fylla sammanslagningsfält i dokumentet med värden från en array av objekt.

Denna metod slår samman data endast för en post. Arrayen med fältnamn och arrayen med värden representerar data för en enda post.

Denna metod använder inte sammanslagningsregioner.

Denna metod ignorerar alternativet [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Exempel



Visar hur man slår samman en bild från en URI som sammanslagningsdata i ett MERGEFIELD.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// MERGEFIELDs med "Image:"‑taggar kommer att få en bild under en sammanslagning.
// Strängen efter kolonet i "Image:"‑taggen motsvarar ett kolumnnamn
// i datakällan vars celler innehåller URI:er till bildfiler.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Skapa en datakälla som innehåller URI:er till bilder som vi ska slå samman.
// En URI kan vara en webbadress som pekar på en bild, eller ett lokalt filsystemfilnamn för en bildfil.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Utför en sammanslagning på en datakälla med en rad.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## Se även

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Utför en koppling från en anpassad datakälla.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Ett objekt som implementerar det anpassade gränssnittet för sammanslagningsdatakälla. |
## Anmärkningar


Använd den här metoden för att fylla sammanslagningsfält i dokumentet med värden från vilken datakälla som helst, såsom en lista, hashtabell eller objekt. Du måste skriva din egen klass som implementerar gränssnittet [IMailMergeDataSource](../../imailmergedatasource/).

Du kan använda den här metoden endast när [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) är **false**, det vill säga när du inte behöver stöd för språk som skrivs från höger till vänster (såsom arabiska eller hebreiska).

Denna metod ignorerar alternativet [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Se även

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
