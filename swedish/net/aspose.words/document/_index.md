---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Document för sömlös hantering av Word-dokument. Förbättra dina projekt med kraftfulla funktioner och enkel integration.
type: docs
weight: 640
url: /sv/net/aspose.words/document/
---
## Document class

Representerar ett Word-dokument.

För att lära dig mer, besök[Arbeta med dokument](https://docs.aspose.com/words/net/working-with-document/) dokumentationsartikel.

```csharp
public class Document : DocumentBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Document](document/#constructor)() | Skapar ett tomt Word-dokument. |
| [Document](document/#constructor_1)(*Stream*) | Öppnar ett befintligt dokument från en ström. Identifierar automatiskt filformatet. |
| [Document](document/#constructor_3)(*string*) | Öppnar ett befintligt dokument från en fil. Identifierar automatiskt filformatet. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Öppnar ett befintligt dokument från en ström. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Öppnar ett befintligt dokument från en fil. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Hämtar eller anger den fullständiga sökvägen till mallen som är bifogad till dokumentet. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Hämtar eller anger en flagga som anger om formaten i dokumentet uppdateras för att matcha formaten i den bifogade mallen varje gång dokumentet öppnas i MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Hämtar eller ställer in dokumentets bakgrundsform. Kan vara`null` . |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | Hämtar[`Bibliography`](./bibliography/)objekt som representerar listan över källor som finns tillgängliga i dokumentet. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Returnerar en samling som representerar alla inbyggda dokumentegenskaper i dokumentet. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Ger åtkomst till dokumentkompatibilitetsalternativ (det vill säga användarinställningarna som angetts på**Kompatibilitet** fliken av**Alternativ**dialogruta i Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Hämtar OOXML-efterlevnadsversionen som bestäms från det laddade dokumentinnehållet. Gäller endast OOXML-dokument. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Returnerar en samling som representerar alla anpassade dokumentegenskaper för dokumentet. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Hämtar eller ställer in samlingen av anpassade XML-datalagringsdelar. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Hämtar eller ställer in intervallet (i punkter) mellan standardtabbstoppen. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Hämtar samlingen av digitala signaturer för detta dokument och deras valideringsresultat. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Hämtar denna instans. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Ger alternativ som styr numrering och placering av slutnoter i det här dokumentet. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Får en[`FieldOptions`](../../aspose.words.fields/fieldoptions/) objekt som representerar alternativ för att styra fälthantering i dokumentet. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Hämtar det första avsnittet i dokumentet. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Ger åtkomst till egenskaper för teckensnitt som används i detta dokument. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Hämtar eller ställer in dokumentets teckensnittsinställningar. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Ger alternativ som styr numrering och placering av fotnoter i det här dokumentet. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Ger åtkomst till fotnots-/slutnotsavgränsare som definierats i dokumentet. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Returnerar en[`Frameset`](./frameset/) exempel om detta dokument representerar en ramsida. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Hämtar eller ställer in ordlistadokumentet i detta dokument eller denna mall. Ett ordlistadokument är ett lagringsutrymme för AutoText-, Autokorrigerings- och Byggblocksposter som definierats i ett dokument. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Returer`sann` om dokumentet har kontrollerats med avseende på grammatik. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Returer`sann` om dokumentet har ett VBA-projekt (makron). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Returer`sann` om dokumentet har några spårade ändringar. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Ger åtkomst till alternativ för avstavning i dokumentet. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Anger om textrutor, fotnoter och slutnoter ska inkluderas i ordräkningsstatistiken. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Hämtar eller ställer in justeringen av teckenavståndet för ett dokument. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Hämtar det sista avsnittet i dokumentet. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Får en[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) objekt som representerar alternativ för att styra layoutprocessen för detta dokument. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Ger åtkomst till listformateringen som används i dokumentet. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Returnerar en[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) objekt som representerar dokumentkopplingsfunktionen för dokumentet. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Hämtar eller anger objektet som innehåller all information om dokumentkoppling för ett dokument. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Anropas när en nod infogas eller tas bort i dokumentet. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | ReturerDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Hämtar dokumentets ursprungliga filnamn. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Hämtar formatet för originaldokumentet som laddades in i det här objektet. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Hämtar eller ställer in samlingen av anpassade delar (godtyckligt innehåll) som är länkade till OOXML-paketet med hjälp av "okända relationer". |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Hämtar eller ställer in dokumentets sidfärg. Den här egenskapen är en enklare version av[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Hämtar antalet sidor i dokumentet beräknat med den senaste sidlayoutoperationen. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Hämtar den aktiva dokumentskyddstypen. |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | Anger om kerning gäller för både latinsk text och interpunktion. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Hämtar eller anger en flagga som anger att Microsoft Word tar bort all användarinformation från kommentarer, revisioner och dokumentegenskaper när dokumentet sparas. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser laddas. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Hämtar en samling revisioner (spårade ändringar) som finns i detta dokument. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Hämtar eller anger ett värde som anger om man ska arbeta med originalversionen eller den reviderade versionen av ett dokument. |
| [Sections](../../aspose.words/document/sections/) { get; } | Returnerar en samling som representerar alla avsnitt i dokumentet. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Anger om grå skuggning ska aktiveras i formulärfält. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Anger om grammatikfel ska visas i det här dokumentet. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Anger om stavfel ska visas i det här dokumentet. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Returer`sann` om dokumentet har stavningskontrollerats. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Returnerar en samling stilar definierade i dokumentet. |
| [Theme](../../aspose.words/document/theme/) { get; } | Hämtar[`Theme`](./theme/) objekt för detta dokument. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | Sant om ändringar spåras när dokumentet redigeras i Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Returnerar samlingen av variabler som lagts till i ett dokument eller en mall. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Hämtar eller ställer in en[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Hämtar antalet dokumentversioner som lagrades i DOC-dokumentet. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Ger alternativ för att styra hur dokumentet visas i Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Anropas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan resultera i förlust av data- eller formateringsåtergivning. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Ger åtkomst till dokumentets vattenstämpel. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Returnerar en samling som representerar en lista med tillägg i åtgärdsfönstret. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Ger åtkomst till dokumentets skrivskyddsalternativ. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Accepterar alla spårade ändringar i dokumentet. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka slutet av dokumentet. |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka början av dokumentet. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Lägger till det angivna dokumentet i slutet av detta dokument. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Lägger till det angivna dokumentet i slutet av detta dokument. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Rensar oanvända format och listor från dokumentet. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Rensar oanvända stilar och listor från dokumentet beroende på angivet[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Utför en djup kopiering av`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Jämför detta dokument med ett annat dokument som producerar ändringar, baserat på antalet redigeringar och formateringsrevisioner.[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Jämför detta dokument med ett annat dokument som producerar ändringar som ett antal redigerings- och formateringsrevisioner[`Revision`](../revision/) . Gör det möjligt att ange jämförelsealternativ med hjälp av[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Kopierar stilar från den angivna mallen till ett dokument. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Kopierar stilar från den angivna mallen till ett dokument. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Om dokumentet inte innehåller några avsnitt skapas ett avsnitt med ett stycke. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Konverterar formatering som anges i tabellformat till direkt formatering på tabeller i dokumentet. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | Returnerar`Document` objekt som representerar ett angivet sidintervall. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Hämtar sidstorlek, orientering och annan information om en sida som kan vara användbar för utskrift eller rendering. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Importerar en nod från ett annat dokument till det aktuella dokumentet. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formateringen. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Kopplar samman körningar med samma formatering i alla stycken i dokumentet. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Ändrar fälttypvärden[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) av[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) i hela dokumentet så att de motsvarar fälttyperna som finns i fältkoderna. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Print](../../aspose.words/document/print/#print)() | Skriver ut hela dokumentet till standardskrivaren. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Skriver ut dokumentet enligt de angivna skrivarinställningarna, med hjälp av standardutskriftskontrollen (inget användargränssnitt). |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Skriv ut hela dokumentet till den angivna skrivaren, med hjälp av standardutskriftskontrollen (inget användargränssnitt). |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Skriver ut dokumentet enligt de angivna skrivarinställningarna, med hjälp av standardutskriftskontrollen (inget användargränssnitt) och ett dokumentnamn. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Skyddar dokumentet från ändringar utan att ändra det befintliga lösenordet eller tilldelar ett slumpmässigt lösenord. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Skyddar dokumentet från ändringar och ställer in ett lösenord om så önskas. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | Tar bort tomma sidor från dokumentet. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Tar bort externa XML-schemareferenser från detta dokument. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Tar bort alla makron (VBA-projektet) samt verktygsfält och kommandoanpassningar från dokumentet. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Återger en dokumentsida till enGraphics objekt i en specificerad skala. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Återger en dokumentsida till enGraphics objekt till en specificerad storlek. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Sparar dokumentet till en fil. Bestämmer automatiskt sparformatet från filändelsen. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Sparar dokumentet till en ström med det angivna formatet. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Sparar dokumentet till en ström med de angivna sparalternativen. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Sparar dokumentet till en fil i det angivna formatet. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Sparar dokumentet till en fil med de angivna sparalternativen. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Skickar dokumentet till klientens webbläsare. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Börjar automatiskt markera alla ytterligare ändringar du gör i dokumentet programmatiskt som revisionsändringar. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Börjar automatiskt markera alla ytterligare ändringar du gör i dokumentet programmatiskt som revisionsändringar. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Stoppar automatisk markering av dokumentändringar som revisioner. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Avlänkar fält i hela dokumentet. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Tar bort skyddet från dokumentet oavsett lösenordet. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Tar bort skyddet från dokumentet om ett korrekt lösenord anges. |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | Uppdaterar[`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/) egenskap för alla fotnoter och slutnoter i dokumentet. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Uppdaterar värdena för fält i hela dokumentet. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Uppdaterar listetiketter för alla listobjekt i dokumentet. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Återskapar dokumentets sidlayout. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Uppdateringar[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) av dokumentet med standardalternativen. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Uppdateringar[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) av dokumentet enligt de angivna alternativen. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Uppdaterar dokumentets egenskaper för ordantal. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Uppdaterar dokumentets ordantal, uppdaterar valfritt[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) egendom. |

## Anmärkningar

De`Document` är ett centralt objekt i Aspose.Words-biblioteket.

För att ladda ett befintligt dokument i någon av[`LoadFormat`](../loadformat/) format, skicka ett filnamn eller en ström till ett av`Document` konstruktorer. För att skapa ett tomt dokument, anropa konstruktorn utan parametrar.

Använd en av överbelastningsmetoderna för att spara dokumentet i någon av [`SaveFormat`](../saveformat/) format.

Att rita dokumentsidor direkt på en**Grafik** objekt use [`RenderToScale`](./rendertoscale/) eller[`RenderToSize`](./rendertosize/) metod.

För att skriva ut dokumentet, använd en av[`Print`](./print/) metoder.

[`MailMerge`](./mailmerge/)är Aspose.Words rapporteringsmotor som gör det möjligt att snabbt och enkelt fylla rapporter utformade i Microsoft Word med data från olika datakällor. Data kan komma från en DataSet, DataTable, DataView, IDataReader eller en array med värden.**Koppla ut e-post** kommer att gå igenom posterna som finns i datakällan och infoga dem i fälten för koppling av dokument i dokumentet och utöka det efter behov.

`Document` lagrar dokumentomfattande information som t.ex.[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) , listor och makron. De flesta av dessa objekt är tillgängliga via motsvarande egenskaper för`Document`.

De`Document` är en rotnod i ett träd som innehåller alla andra noder i dokumentet. Trädet är ett sammansatt designmönster och på många sätt likt XmlDocument. Dokumentets innehåll kan manipuleras fritt programmatiskt:

* Dokumentets noder kan nås via typade samlingar, till exempel[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) etc.
* Dokumentets noder kan väljas utifrån deras nodtyp med hjälp av [`GetChildNodes`](../compositenode/getchildnodes/) eller med hjälp av en XPath-fråga med[`SelectNodes`](../compositenode/selectnodes/) eller[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Innehållsnoder kan läggas till eller tas bort var som helst i dokumentet med hjälp av [`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) och andra -metoder som tillhandahålls av basklassen[`CompositeNode`](../compositenode/).
* Formateringsattributen för varje nod kan ändras via nodens egenskaper.

Överväg att använda[`DocumentBuilder`](../documentbuilder/) det förenklar uppgiften att programmatiskt skapa eller fylla i dokumentträdet.

De`Document` kan endast innehålla[`Section`](../section/) föremål.

I Microsoft Word måste ett giltigt dokument ha minst ett avsnitt.

## Exempel

Visar hur man utför en dokumentkoppling med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan följer två sätt att använda en datatabell som datakälla för en dokumentkoppling.
    // 1 - Använd hela tabellen för dokumentkopplingen för att skapa ett utgående dokumentkopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett enda dokument för koppling av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för dokumentkoppling.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Se även

* class [DocumentBase](../documentbase/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
