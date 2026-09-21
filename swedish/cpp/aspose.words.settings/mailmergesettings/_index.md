---
title: "Aspose::Words::Settings::MailMergeSettings klass"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::MailMergeSettings klass. Anger all mail merge‑information för ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Anger all information för mail merge i ett dokument. För att läsa mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Rensar mail merge‑inställningarna på ett sätt så att när dokumentet sparas, sparas inga mail merge‑inställningar och det blir ett vanligt dokument. |
| [Clone](./clone/)() | Returnerar en djup klon av detta objekt. |
| [get_ActiveRecord](./get_activerecord/)() const | Anger det ettbaserade indexet för posten från datakällan som ska visas i Microsoft Word. Standardvärdet är 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Anger kolumnen i datakällan som innehåller e‑postadresser. Standardvärdet är en tom sträng. |
| [get_CheckErrors](./get_checkerrors/)() const | Anger typen av felrapportering som Microsoft Word ska utföra vid en mail merge. Standardvärdet är [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Anger anslutningssträngen som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |
| [get_DataSource](./get_datasource/)() const | Anger sökvägen till mail‑merge‑datakällan. Standardvärdet är en tom sträng. |
| [get_DataType](./get_datatype/)() const | Anger typen av mail‑merge‑datakälla och metoden för dataåtkomst. Standardvärdet är [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Anger hur Microsoft Word kommer att leverera resultaten av en mail merge. Standardvärdet är [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Anger hur ett program som utför mail merge ska hantera tomma rader i de sammanslagna dokumenten som resultat av mail merge. Standardvärdet är **false**. |
| [get_HeaderSource](./get_headersource/)() const | Anger sökvägen till mail‑merge‑huvudkällan. Standardvärdet är en tom sträng. |
| [get_LinkToQuery](./get_linktoquery/)() const | Inte säker på den här. Microsoft Word Automation Reference föreslår att detta anger att frågan körs varje gång dokumentet öppnas i Microsoft Word. Men OOXML-specifikationen föreslår att detta anger att frågan innehåller en referens till en extern frågefil som innehåller den faktiska frågan. Standardvärdet är **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Anger att dokumenten som skapas under en kopplingssammanfogning ska skickas som en bilaga snarare än i själva e-postmeddelandets brödtext. Standardvärdet är **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Anger den text som ska visas i ämnesraden för e‑postmeddelanden eller fax som produceras under kopplingssammanfogning. Standardvärdet är en tom sträng. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Anger huvuddokumenttypen för kopplingssammanfogning. Standardvärdet är [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Hämtar objektet som anger inställningarna för Office Data Source Object (ODSO). |
| [get_Query](./get_query/)() const | Innehåller Structured Query Language-strängen som ska köras mot den angivna externa datakällan för att returnera den uppsättning poster som ska importeras till dokumentet när kopplingssammanfogningen utförs. Standardvärdet är en tom sträng. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Anger att Microsoft Word ska visa data från den angivna externa datakällan där sammanslagningsfält har infogats (t.ex. förhandsgranska sammanslagna data). Standardvärdet är **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Anger det ettbaserade indexet för posten från datakällan som ska visas i Microsoft Word. Standardvärdet är 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Anger kolumnen i datakällan som innehåller e‑postadresser. Standardvärdet är en tom sträng. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Anger typen av felrapportering som Microsoft Word ska utföra vid en mail merge. Standardvärdet är [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Anger anslutningssträngen som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Anger sökvägen till mail‑merge‑datakällan. Standardvärdet är en tom sträng. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Anger typen av mail‑merge‑datakälla och metoden för dataåtkomst. Standardvärdet är [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Anger hur Microsoft Word kommer att leverera resultaten av en mail merge. Standardvärdet är [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Anger hur ett program som utför mail merge ska hantera tomma rader i de sammanslagna dokumenten som resultat av mail merge. Standardvärdet är **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Anger sökvägen till mail‑merge‑huvudkällan. Standardvärdet är en tom sträng. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | Sättare för [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Anger att dokumenten som skapas under en kopplingssammanfogning ska skickas som en bilaga snarare än i själva e-postmeddelandets brödtext. Standardvärdet är **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Anger den text som ska visas i ämnesraden för e‑postmeddelanden eller fax som produceras under kopplingssammanfogning. Standardvärdet är en tom sträng. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | Sättare för [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Ställer in objektet som anger inställningarna för Office Data Source Object (ODSO). |
| [set_Query](./set_query/)(const System::String\&) | Innehåller Structured Query Language-strängen som ska köras mot den angivna externa datakällan för att returnera den uppsättning poster som ska importeras till dokumentet när kopplingssammanfogningen utförs. Standardvärdet är en tom sträng. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Anger att Microsoft Word ska visa data från den angivna externa datakällan där sammanslagningsfält har infogats (t.ex. förhandsgranska sammanslagna data). Standardvärdet är **false**. |
| static [Type](./type/)() |  |
## Anmärkningar


Du kan använda detta objekt för att ange en datakälla för kopplingssammanfogning för ett dokument och denna information (tillsammans med de tillgängliga datafälten) kommer att visas i Microsoft Word när användaren öppnar dokumentet. Eller så kan du använda detta objekt för att fråga efter kopplingssammanfogningsinställningar som användaren har angett i Microsoft Word för detta dokument.

Du behöver normalt inte skapa objekt av den här klassen direkt eftersom kopplingssammanfogningsinställningarna för ett dokument alltid är tillgängliga via egenskapen [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/).

För att upptäcka om detta dokument är ett huvuddokument för kopplingssammanfogning, kontrollera värdet på egenskapen [MainDocumentType](./get_maindocumenttype/).

För att ta bort kopplingssammanfogningsinställningar och information om datakälla från ett dokument kan du använda metoden [Clear](./clear/). Aspose.Words kommer inte att skriva kopplingssammanfogningsinställningar till ett dokument om egenskapen [MainDocumentType](./get_maindocumenttype/) är satt till [NotAMergeDocument](../mailmergemaindocumenttype/) eller egenskapen [DataType](./get_datatype/) är satt till [None](../mailmergedatatype/).

Det bästa sättet att lära sig hur man använder egenskaperna för detta objekt är att skapa ett dokument med en önskad datakälla manuellt i Microsoft Word och sedan öppna det dokumentet med Aspose.Words och undersöka egenskaperna för objekten [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) och [Odso](./get_odso/). Detta är ett bra tillvägagångssätt om du till exempel vill lära dig hur man programatiskt konfigurerar en datakälla.

Aspose.Words bevarar information om kopplad utskick när dokument laddas, sparas och konverteras mellan olika format, men använder inte denna information när den utför sin egen kopplade utskick med hjälp av objektet [MailMerge](../../aspose.words.mailmerging/mailmerge/).

## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
