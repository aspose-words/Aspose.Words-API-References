---
title: Document
second_title: Aspose.Words för .NET API Referens
description: Representerar ett Word-dokument.
type: docs
weight: 420
url: /sv/net/aspose.words/document/
---
## Document class

Representerar ett Word-dokument.

```csharp
public class Document : DocumentBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Document](document#constructor)() | Skapar ett tomt Word-dokument. |
| [Document](document#constructor_1)(Stream) | Öppnar ett befintligt dokument från en ström. Upptäcker automatiskt filformatet. |
| [Document](document#constructor_3)(string) | Öppnar ett befintligt dokument från en fil. Upptäcker automatiskt filformatet. |
| [Document](document#constructor_2)(Stream, LoadOptions) | Öppnar ett befintligt dokument från en ström. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord. |
| [Document](document#constructor_4)(string, LoadOptions) | Öppnar ett befintligt dokument från en fil. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate) { get; set; } | Hämtar eller ställer in hela sökvägen för mallen som är bifogad till dokumentet. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles) { get; set; } | Hämtar eller ställer in en flagga som anger om stilarna i dokumentet uppdateras för att matcha stilarna i den bifogade mallen varje gång dokumentet öppnas i MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Hämtar eller ställer in bakgrundsformen för dokumentet. Kan vara null. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties) { get; } | Returnerar en samling som representerar alla inbyggda dokumentegenskaper i dokumentet. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Hämtar alla omedelbara underordnade noder för denna nod. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions) { get; } | Ger tillgång till dokumentkompatibilitetsalternativ (det vill säga användarinställningarna som anges på **Kompatibilitet** fliken i **alternativ** dialog i Word). |
| [Compliance](../../aspose.words/document/compliance) { get; } | Får OOXML-kompatibilitetsversionen fastställd från det inlästa dokumentinnehållet. Är meningsfullt endast för OOXML-dokument. |
| [Count](../../aspose.words/compositenode/count) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties) { get; } | Returnerar en samling som representerar alla anpassade dokumentegenskaper för dokumentet. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Anger anpassad nodidentifierare. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts) { get; set; } | Hämtar eller ställer in samlingen av anpassade XML-datalagringsdelar. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop) { get; set; } | Hämtar eller ställer in intervallet (i poäng) mellan standardtabbstoppen. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures) { get; } | Hämtar insamlingen av digitala signaturer för detta dokument och deras valideringsresultat. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions) { get; } | Ger alternativ som styr numrering och placering av slutnoter i detta dokument. |
| [FieldOptions](../../aspose.words/document/fieldoptions) { get; } | Får en **Fältalternativ**objekt som representerar alternativ för att styra fälthanteringen i dokumentet. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Får det första barnet i noden. |
| [FirstSection](../../aspose.words/document/firstsection) { get; } | Hämtar det första avsnittet i dokumentet. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Ger tillgång till egenskaperna för teckensnitt som används i detta dokument. |
| [FontSettings](../../aspose.words/document/fontsettings) { get; set; } | Hämtar eller ställer in dokumentfontinställningar. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions) { get; } | Ger alternativ som styr numrering och placering av fotnoter i detta dokument. |
| [Frameset](../../aspose.words/document/frameset) { get; } | Returnerar en[`Frameset`](./frameset)instans om detta dokument representerar en ramsida. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument) { get; set; } | Hämtar eller ställer in ordlistans dokument i detta dokument eller mall. Ett ordlistadokument är en storage för AutoText, AutoCorrect och Building Block-poster definierade i ett dokument. |
| [GrammarChecked](../../aspose.words/document/grammarchecked) { get; set; } | Returnerar **Sann** om dokumentet har kontrollerats för grammatik. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returnerar sant om denna nod har några underordnade noder. |
| [HasMacros](../../aspose.words/document/hasmacros) { get; } | Returnerar **Sann** om dokumentet har ett VBA-projekt (makron). |
| [HasRevisions](../../aspose.words/document/hasrevisions) { get; } | Returnerar **Sann** om dokumentet har några spårade ändringar. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions) { get; } | Ger tillgång till alternativ för dokumentavstavning. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returnerar sant eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Hämtar nodens sista underordnade. |
| [LastSection](../../aspose.words/document/lastsection) { get; } | Hämtar det sista avsnittet i dokumentet. |
| [LayoutOptions](../../aspose.words/document/layoutoptions) { get; } | Får en **Layoutalternativ** objekt som representerar alternativ för att styra layoutprocessen för detta dokument. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Ger tillgång till listformateringen som används i dokumentet. |
| [MailMerge](../../aspose.words/document/mailmerge) { get; } | Returnerar en **MailMerge** objekt som representerar kopplingsfunktionen för dokumentet. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings) { get; set; } | Hämtar eller ställer in objektet som innehåller all kopplingsinformation för ett dokument. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Hämtar noden omedelbart efter denna nod. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Anropas när en nod infogas eller tas bort i dokumentet. |
| override [NodeType](../../aspose.words/document/nodetype) { get; } | Returnerar **NodeType.Document** . |
| [OriginalFileName](../../aspose.words/document/originalfilename) { get; } | Hämtar originalfilnamnet för dokumentet. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat) { get; } | Hämtar formatet för originaldokumentet som laddades in i detta objekt. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts) { get; set; } | Hämtar eller ställer in samlingen av anpassade delar (godtyckligt innehåll) som är länkade till OOXML-paketet med hjälp av "okända relationer". |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Hämtar eller ställer in sidfärgen på dokumentet. Den här egenskapen är en enklare version av[`BackgroundShape`](../documentbase/backgroundshape) . |
| [PageCount](../../aspose.words/document/pagecount) { get; } | Hämtar antalet sidor i dokumentet som beräknats av den senaste sidlayoutoperationen. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Hämtar noden omedelbart före denna nod. |
| [ProtectionType](../../aspose.words/document/protectiontype) { get; } | Får den för närvarande aktiva dokumentskyddstypen. |
| [Range](../../aspose.words/node/range) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation) { get; set; } | Hämtar eller ställer in en flagga som indikerar att Microsoft Word kommer att ta bort all användarinformation från kommentarer, revisioner och dokumentegenskaper när dokumentet sparas. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Gör det möjligt att styra hur externa resurser laddas. |
| [Revisions](../../aspose.words/document/revisions) { get; } | Hämtar en samling revisioner (spårade ändringar) som finns i detta dokument. |
| [RevisionsView](../../aspose.words/document/revisionsview) { get; set; } | Hämtar eller ställer in ett värde som indikerar om man ska arbeta med den ursprungliga eller reviderade versionen av ett dokument. |
| [Sections](../../aspose.words/document/sections) { get; } | Returnerar en samling som representerar alla avsnitt i dokumentet. |
| [ShadeFormData](../../aspose.words/document/shadeformdata) { get; set; } | Anger om den grå skuggningen ska aktiveras i formulärfält. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors) { get; set; } | Anger om grammatikfel ska visas i detta dokument. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors) { get; set; } | Anger om stavfel ska visas i detta dokument. |
| [SpellingChecked](../../aspose.words/document/spellingchecked) { get; set; } | Returnerar **Sann** om dokumentet har stavningskontrollerats. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Returnerar en samling stilar definierade i dokumentet. |
| [Theme](../../aspose.words/document/theme) { get; } | Får[`Theme`](./theme) objekt för detta dokument. |
| [TrackRevisions](../../aspose.words/document/trackrevisions) { get; set; } | **Sann** om ändringar spåras när detta dokument redigeras i Microsoft Word. |
| [Variables](../../aspose.words/document/variables) { get; } | Returnerar samlingen av variabler som lagts till i ett dokument eller mall. |
| [VbaProject](../../aspose.words/document/vbaproject) { get; set; } | Hämtar eller sätter en[`VbaProject`](./vbaproject) . |
| [VersionsCount](../../aspose.words/document/versionscount) { get; } | Hämtar antalet dokumentversioner som lagrades i DOC-dokumentet. |
| [ViewOptions](../../aspose.words/document/viewoptions) { get; } | Ger alternativ för att styra hur dokumentet visas i Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Anropas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan resultera i data- eller formateringsförlust. |
| [Watermark](../../aspose.words/document/watermark) { get; } | Ger åtkomst till dokumentets vattenstämpel. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes) { get; } | Returnerar en samling som representerar en lista över tillägg i aktivitetsfönstret. |
| [WriteProtection](../../aspose.words/document/writeprotection) { get; } | Ger åtkomst till alternativen för dokumentskrivskydd. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/document/accept)(DocumentVisitor) | Accepterar en besökare. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions)() | Accepterar alla spårade ändringar i dokumentet. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument)(Document, ImportFormatMode) | Lägger till det angivna dokumentet i slutet av detta dokument. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Lägger till det angivna dokumentet i slutet av detta dokument. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup)() | Rensar oanvända stilar och listor från dokumentet. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup_1)(CleanupOptions) | Rensar oanvända stilar och listor från dokumentet beroende på givet[`CleanupOptions`](../cleanupoptions) . |
| [Clone](../../aspose.words/document/clone#clone)() | Utför en djup kopia av[`Document`](../document) . |
| [Clone](../../aspose.words/node/clone)(bool) | Skapar en dubblett av noden. |
| [Compare](../../aspose.words/document/compare#compare)(Document, string, DateTime) | Jämför detta dokument med ett annat dokument som ger ändringar som antal redigeringar och formatrevisioner[`Revision`](../revision) . |
| [Compare](../../aspose.words/document/compare#compare_1)(Document, string, DateTime, CompareOptions) | Jämför detta dokument med ett annat dokument som ger ändringar som ett antal redigerings- och formatrevisioner[`Revision`](../revision) . Gör det möjligt att ange jämförelsealternativ med hjälp av[`CompareOptions`](../../aspose.words.comparing/compareoptions) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate)(Document) | Kopierar stilar från den angivna mallen till ett dokument. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate_1)(string) | Kopierar stilar från den angivna mallen till ett dokument. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserverad för systemanvändning. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum)() | Om dokumentet inte innehåller några avsnitt skapas ett avsnitt med ett stycke. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting)() | Konverterar formatering som anges i tabellstilar till direkt formatering på tabeller i dokumentet. |
| [ExtractPages](../../aspose.words/document/extractpages)(int, int) | Returnerar[`Document`](../document) objekt som representerar specificerat intervall av sidor. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| [GetPageInfo](../../aspose.words/document/getpageinfo)(int) | Hämtar sidstorlek, orientering och annan information om en sida som kan vara användbar för utskrift eller rendering. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Hämtar texten för denna nod och alla dess underordnade. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool) | Importerar en nod från ett annat dokument till det aktuella dokumentet. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool, ImportFormatMode) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formateringen. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting)() | Sammanfogar körningar med samma formatering i alla stycken i dokumentet. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes)() | Ändrar fälttypvärden[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype) av[`FieldStart`](../../aspose.words.fields/fieldstart) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator) ,[`FieldEnd`](../../aspose.words.fields/fieldend) i hela dokumentet så att de motsvarar fälttyperna som finns i fältkoderna. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Print](../../aspose.words/document/print#print)() | Skriver ut hela dokumentet till standardskrivaren. |
| [Print](../../aspose.words/document/print#print_1)(PrinterSettings) | Skriver ut dokumentet enligt de angivna skrivarinställningarna, med standardutskriftskontrollern (utan användargränssnitt). |
| [Print](../../aspose.words/document/print#print_3)(string) | Skriv ut hela dokumentet till den angivna skrivaren, med standardutskriftskontrollern (inget användargränssnitt). |
| [Print](../../aspose.words/document/print#print_2)(PrinterSettings, string) | Skriver ut dokumentet enligt de angivna skrivarinställningarna, med standardutskriftskontrollern (inget användargränssnitt) och ett dokumentnamn. |
| [Protect](../../aspose.words/document/protect#protect)(ProtectionType) | Skyddar dokumentet från ändringar utan att ändra det befintliga lösenordet eller tilldelar ett slumpmässigt lösenord. |
| [Protect](../../aspose.words/document/protect#protect_1)(ProtectionType, string) | Skyddar dokumentet från ändringar och anger valfritt ett skyddslösenord. |
| [Remove](../../aspose.words/node/remove)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Tar bort den angivna underordnade noden. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences)() | Tar bort externa XML-schemareferenser från detta dokument. |
| [RemoveMacros](../../aspose.words/document/removemacros)() | Tar bort alla makron (VBA-projektet) samt verktygsfält och kommandoanpassningar från dokumentet. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag) underliggande noder till den aktuella noden. |
| [RenderToScale](../../aspose.words/document/rendertoscale)(int, Graphics, float, float, float) | Gör en dokumentsida till enGraphics objekt i en angiven skala. |
| [RenderToSize](../../aspose.words/document/rendertosize)(int, Graphics, float, float, float, float) | Gör en dokumentsida till enGraphics objekt till en angiven storlek. |
| [Save](../../aspose.words/document/save#save_2)(string) | Sparar dokumentet till en fil. Bestämmer automatiskt sparformatet från tillägget. |
| [Save](../../aspose.words/document/save#save)(Stream, SaveFormat) | Sparar dokumentet i en ström med det angivna formatet. |
| [Save](../../aspose.words/document/save#save_1)(Stream, SaveOptions) | Sparar dokumentet i en ström med de angivna sparalternativen. |
| [Save](../../aspose.words/document/save#save_3)(string, SaveFormat) | Sparar dokumentet till en fil i angivet format. |
| [Save](../../aspose.words/document/save#save_4)(string, SaveOptions) | Sparar dokumentet till en fil med de angivna sparalternativen. |
| [Save](../../aspose.words/document/save#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Skickar dokumentet till klientens webbläsare. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Väljer den första noden som matchar XPath-uttrycket. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions)(string) | Börjar automatiskt markera alla ytterligare ändringar du gör i dokumentet programmatiskt som revisionsändringar. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions_1)(string, DateTime) | Börjar automatiskt markera alla ytterligare ändringar du gör i dokumentet programmatiskt som revisionsändringar. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions)() | Stoppar automatisk markering av dokumentändringar som revisioner. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| [UnlinkFields](../../aspose.words/document/unlinkfields)() | Tar bort länkar till fält i hela dokumentet. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect_1)() | Tar bort skyddet från dokumentet oavsett lösenord. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect)(string) | Tar bort skyddet från dokumentet om ett korrekt lösenord anges. |
| [UpdateFields](../../aspose.words/document/updatefields)() | Uppdaterar värdena för fält i hela dokumentet. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels)() | Uppdaterar listetiketter för alla listobjekt i dokumentet. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout)() | Bygger om dokumentets sidlayout. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail)() | Uppdateringar[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) av dokumentet med standardalternativ. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail_1)(ThumbnailGeneratingOptions) | Uppdateringar[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) av dokumentet enligt de angivna alternativen. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount)() | Uppdaterar ordräkningsegenskaper för dokumentet. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount_1)(bool) | Uppdaterar ordräkningsegenskaper för dokumentet, uppdaterar eventuellt[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines) egenskap. |

### Anmärkningar

De **Dokumentera** är ett centralt objekt i Aspose.Words-biblioteket.

För att ladda ett befintligt dokument i någon av[`LoadFormat`](../loadformat) format, skicka ett filnamn eller en ström till en av **Dokumentera** konstruktörer. För att skapa ett tomt dokument, anropa konstruktorn utan parametrar.

Använd en av överbelastningsmetoderna för att spara dokumentet i någon av the [`SaveFormat`](../saveformat) format.

Att rita dokumentsidor direkt på en **Grafik** objekt användning [`RenderToScale`](./rendertoscale) eller[`RenderToSize`](./rendertosize) metod.

För att skriva ut dokumentet, använd en av[`Print`](./print)metoder.

[`MailMerge`](./mailmerge) är Aspose.Words rapportmotor som gör det möjligt att snabbt och enkelt fylla rapporter designade i Microsoft Word med data från olika datakällor. Datan kan vara från en Dataset, DataTable, DataView, IDataReader eller en uppsättning värden.  **MailMerge** kommer att gå igenom posterna som finns i datakällan och infoga dem i e-postsammanslagningsfält i dokumentet och utöka det vid behov.

**Dokumentera** lagrar dokumentövergripande information som t.ex[`Styles`](../documentbase/styles) , [`BuiltInDocumentProperties`](./builtindocumentproperties) ,[`CustomDocumentProperties`](./customdocumentproperties) , listor och makron. De flesta av dessa objekt är tillgängliga via motsvarande egenskaper för **Dokumentera**.

De **Dokumentera**är en rotnod i ett träd som innehåller alla andra noder i dokumentet. Trädet är ett sammansatt designmönster och på många sätt liknar XmlDocument. Innehållet i dokumentet kan manipuleras fritt programmatiskt:

* Dokumentets noder kan till exempel nås via maskinskrivna samlingar[`Sections`](./sections) , [`ParagraphCollection`](../paragraphcollection) etc.
* Dokumentets noder kan väljas efter deras nodtyp med hjälp av [`GetChildNodes`](../compositenode/getchildnodes) eller använda en XPath-fråga med[`SelectNodes`](../compositenode/selectnodes) eller[`SelectSingleNode`](../compositenode/selectsinglenode).
* Innehållsnoder kan läggas till eller tas bort från var som helst i dokumentet med [`InsertBefore`](../compositenode/insertbefore) ,[`InsertAfter`](../compositenode/insertafter) , [`RemoveChild`](../compositenode/removechild) och andra metoder som tillhandahålls av basklassen[`CompositeNode`](../compositenode).
* Formateringsattributen för varje nod kan ändras via egenskaperna för den noden.

Överväg att använda[`DocumentBuilder`](../documentbuilder) som förenklar uppgiften att programmatiskt skapa eller fylla i dokumentträdet.

De **Dokumentera** kan endast innehålla[`Section`](../section) objekt.

I Microsoft Word måste ett giltigt dokument ha minst ett avsnitt.

### Exempel

Visar hur man kör en e-postsammanfogning med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan finns två sätt att använda en datatabell som datakälla för en e-postkoppling.
    // 1 - Använd hela tabellen för kopplingen för att skapa ett kopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett dokument för utmatning av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för sammankoppling av brev.
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

* class [DocumentBase](../documentbase)
* namnutrymme [Aspose.Words](../../aspose.words)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
