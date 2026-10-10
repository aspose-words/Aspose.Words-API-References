---
title: "Aspose::Words::Document-klass"
linktitle: "Dokument"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document-klass. Representerar ett Word-dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words/document/
---
## Document class


Representerar ett Word-dokument. För att läsa mer, besök dokumentationsartikeln [Arbeta med dokument](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Accepterar alla spårade ändringar i dokumentet. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka dokumentets slut. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka dokumentets början. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Lägger till det angivna dokumentet i slutet av detta dokument. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Lägger till det angivna dokumentet i slutet av detta dokument. |
| [Cleanup](./cleanup/)() | Rensar oanvända stilar och listor från dokumentet. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Rensar oanvända stilar och listor från dokumentet beroende på angivna [CleanupOptions](../cleanupoptions/). |
| [Clone](./clone/)() | Utför en djup kopiering av [Document](./). |
| [Clone](../node/clone/)(bool) | Skapar en kopia av noden. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Jämför detta dokument med ett annat dokument och producerar förändringar som antal redigerings- och formateringsrevisioner [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Jämför detta dokument med ett annat dokument och producerar förändringar som ett antal redigerings- och formateringsrevisioner [Revision](../revision/). Tillåter att specificera jämförelsealternativ med hjälp av [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Kopierar stilar från den angivna mallen till ett dokument. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Kopierar stilar från den angivna mallen till ett dokument. |
| [Document](./document/)() | Skapar ett tomt Word-dokument. |
| [Document](./document/)(const System::String\&) | Öppnar ett befintligt dokument från en fil. Detekterar automatiskt filformatet. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Öppnar ett befintligt dokument från en fil. Tillåter att specificera ytterligare alternativ såsom ett krypteringslösenord. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Öppnar ett befintligt dokument från en ström. Detekterar automatiskt filformatet. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Öppnar ett befintligt dokument från en ström. Tillåter att specificera ytterligare alternativ såsom ett krypteringslösenord. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Om dokumentet inte innehåller några sektioner, skapas en sektion med ett stycke. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Konverterar formatering som anges i tabellstilar till direkt formatering på tabeller i dokumentet. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Returnerar [Document](./)-objektet som representerar det angivna sidintervallet och de givna extraheringsalternativen för sidor. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Returnerar [Document](./) objektet som representerar det angivna intervallet av sidor. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Hämtar eller anger den fullständiga sökvägen till mallen som är bifogad dokumentet. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Hämtar eller anger en flagga som indikerar om stilarna i dokumentet uppdateras för att matcha stilarna i den bifogade mallen varje gång dokumentet öppnas i MS Word. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Hämtar eller anger bakgrundsformen för dokumentet. Kan vara **null**. |
| [get_Bibliography](./get_bibliography/)() | Hämtar [Bibliography](./get_bibliography/)-objektet som representerar listan över källor som finns i dokumentet. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Returnerar en samling som representerar alla inbyggda dokumentegenskaper för dokumentet. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Tillhandahåller åtkomst till dokumentets kompatibilitetsalternativ (det vill säga användarinställningarna som anges på fliken **Compatibility** i **Options**-dialogrutan i Word). |
| [get_Compliance](./get_compliance/)() | Hämtar OOXML‑kompatibilitetsversionen som bestäms utifrån det inlästa dokumentets innehåll. Är bara meningsfull för OOXML‑dokument. |
| [get_Count](../compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Returnerar en samling som representerar alla anpassade dokumentegenskaper för dokumentet. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Hämtar eller anger samlingen av Custom XML Data Storage Parts. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Hämtar eller anger intervallet (i punkter) mellan standardtabbstopp. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Hämtar samlingen av digitala signaturer för detta dokument och deras valideringsresultat. |
| [get_Document](../documentbase/get_document/)() const override | Hämtar denna instans. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Tillhandahåller alternativ som styr numrering och placering av slutnoter i detta dokument. |
| [get_FieldOptions](./get_fieldoptions/)() | Hämtar ett [FieldOptions](../../aspose.words.fields/fieldoptions/)-objekt som representerar alternativ för att kontrollera fältbehandling i dokumentet. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FirstSection](./get_firstsection/)() | Hämtar den första sektionen i dokumentet. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Tillhandahåller åtkomst till egenskaper för teckensnitt som används i detta dokument. |
| [get_FontSettings](./get_fontsettings/)() const | Hämtar eller anger dokumentets teckensnittinställningar. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Tillhandahåller alternativ som styr numrering och placering av fotnoter i detta dokument. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Tillhandahåller åtkomst till fotnot-/slutnotseparatorerna som definierats i dokumentet. |
| [get_Frameset](./get_frameset/)() const | Returnerar en [Frameset](./get_frameset/)-instans om detta dokument representerar en ram-sida. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Hämtar eller anger glossariedokumentet inom detta dokument eller mall. Ett glossariedokument är en lagring för AutoText-, AutoCorrect- och Building Block‑poster som definierats i ett dokument. |
| [get_GrammarChecked](./get_grammarchecked/)() | Returnerar **true** om dokumentet har kontrollerats för grammatik. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_HasMacros](./get_hasmacros/)() | Returnerar **true** om dokumentet har ett VBA‑projekt (makron). |
| [get_HasRevisions](./get_hasrevisions/)() | Returnerar **true** om dokumentet har några spårade ändringar. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Tillhandahåller åtkomst till dokumentets avstavningsalternativ. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Anger om textrutor, fotnoter och slutnoter ska inkluderas i ordantalstatistik. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_JustificationMode](./get_justificationmode/)() | Hämtar eller anger teckenavståndsjusteringen för ett dokument. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_LastSection](./get_lastsection/)() | Hämtar den sista sektionen i dokumentet. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Hämtar ett [LayoutOptions](../../aspose.words.layout/layoutoptions/)‑objekt som representerar alternativ för att styra layoutprocessen för detta dokument. |
| [get_Lists](../documentbase/get_lists/)() const | Tillhandahåller åtkomst till listformateringen som används i dokumentet. |
| [get_MailMerge](./get_mailmerge/)() | Returnerar ett [MailMerge](../../aspose.words.mailmerging/mailmerge/)‑objekt som representerar e-postsammanfogningsfunktionen för dokumentet. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Hämtar eller anger objektet som innehåller all e-postsammanfogningsinformation för ett dokument. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Kallas när en nod infogas eller tas bort i dokumentet. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | Hämtar det ursprungliga filnamnet för dokumentet. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Hämtar formatet för det ursprungliga dokumentet som laddades in i detta objekt. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Hämtar eller anger samlingen av anpassade delar (godtyckligt innehåll) som är länkade till OOXML‑paketet med hjälp av \"okända relationer\". |
| [get_PageColor](../documentbase/get_pagecolor/)() | Hämtar eller anger sidans färg i dokumentet. Denna egenskap är en enklare version av [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | Hämtar antalet sidor i dokumentet enligt den senaste sidlayoutoperationen. |
| [get_ParentNode](../node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Hämtar den för närvarande aktiva dokumentskyddstypen. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Anger om kerning gäller både latinsk text och interpunktion. |
| [get_Range](../node/get_range/)() | Returnerar ett [Range](../range/)-objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Tillhandahåller information om läsbarhetspoäng för dokumentet. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Hämtar eller anger en flagga som indikerar att Microsoft Word kommer att ta bort all användarinformation från kommentarer, revisioner och dokumentegenskaper när dokumentet sparas. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Tillåter att styra hur externa resurser laddas. |
| [get_Revisions](./get_revisions/)() | Hämtar en samling av revisioner (spårade ändringar) som finns i detta dokument. |
| [get_RevisionsView](./get_revisionsview/)() const | Hämtar eller anger ett värde som indikerar om man ska arbeta med den ursprungliga eller reviderade versionen av ett dokument. |
| [get_Sections](./get_sections/)() | Returnerar en samling som representerar alla sektioner i dokumentet. |
| [get_ShadeFormData](./get_shadeformdata/)() | Anger om grå skuggning på formulärfält ska slås på. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Anger om grammatikfel ska visas i detta dokument. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Anger om stavfel ska visas i detta dokument. |
| [get_SpellingChecked](./get_spellingchecked/)() | Returnerar **true** om dokumentet har kontrollerats för stavning. |
| [get_Styles](../documentbase/get_styles/)() const | Returnerar en samling av stilar som definierats i dokumentet. |
| [get_Theme](./get_theme/)() | Hämtar [Theme](./get_theme/) objektet för detta dokument. |
| [get_TrackRevisions](./get_trackrevisions/)() | Sant om ändringar spåras när detta dokument redigeras i Microsoft Word. |
| [get_Variables](./get_variables/)() | Returnerar samlingen av variabler som lagts till i ett dokument eller en mall. |
| [get_VbaProject](./get_vbaproject/)() const | Hämtar eller anger ett [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Hämtar antalet dokumentversioner som lagrades i DOC‑dokumentet. |
| [get_ViewOptions](./get_viewoptions/)() | Tillhandahåller alternativ för att styra hur dokumentet visas i Microsoft Word. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Kallas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan leda till förlust av data‑ eller formateringsnoggrannhet. |
| [get_Watermark](./get_watermark/)() | Tillhandahåller åtkomst till dokumentets vattenstämpel. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Returnerar en samling som representerar en lista över tillägg för uppgiftspanelen. |
| [get_WriteProtection](./get_writeprotection/)() | Tillhandahåller åtkomst till dokumentets skrivskyddsalternativ. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern till den angivna [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Hämtar sidstorlek, orientering och annan information om en sida som kan vara användbar för utskrift eller rendering. |
| [GetText](../compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importerar en nod från ett annat dokument till det aktuella dokumentet. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formatering. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formatering. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar indexet för den angivna barnnoden i barnnodarrayen. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Slår ihop runs med samma formatering i alla stycken i dokumentet. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Ändrar fälttypvärden [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) för [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) i hela dokumentet så att de motsvarar de fälttyper som finns i fältkoderna. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Skyddar dokumentet mot ändringar utan att ändra det befintliga lösenordet eller tilldelar ett slumpmässigt lösenord. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Skyddar dokumentet mot ändringar och kan valfritt ange ett skyddslösenord. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Tar bort alla barnnoder för den aktuella noden. |
| [RemoveBlankPages](./removeblankpages/)() | Tar bort tomma sidor från dokumentet. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Tar bort verktygsfält och anpassade tangentbordskommandon från dokumentet. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Tar bort externa XML‑schemareferenser från detta dokument. |
| [RemoveMacros](./removemacros/)() | Tar bort alla makron (VBA‑projektet) samt verktygsfält och kommandotillpassningar från dokumentet. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Tar bort alla [SmartTag](../../aspose.words.markup/smarttag/)‑nedärvda noder för den aktuella noden. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderar en dokumentsida till ett **Graphics**‑objekt i en angiven skala. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Ritar en dokumentsida till ett **Graphics**-objekt i en specificerad storlek. |
| [Save](./save/)(const System::String\&) | Sparar dokumentet till en fil. Bestämmer automatiskt sparformatet från filändelsen. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Sparar dokumentet till en fil i det angivna formatet. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Sparar dokumentet till en fil med de angivna sparalternativen. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Sparar dokumentet till en ström med det angivna formatet. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Sparar dokumentet till en ström med de angivna sparalternativen. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../node/) som matchar XPath‑uttrycket. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Sättare för [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Sättare för [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Sättare för [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Sättare för [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Sättare för [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Sättare för [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Sättare för [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Sättare för [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Sättare för [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Sättare för [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Sättare för [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Kallas när en nod infogas eller tas bort i dokumentet. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Sättare för [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Sättare för [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Sättare för [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Sättare för [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Tillåter att styra hur externa resurser laddas. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Sättare för [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Sättare för [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Sättare för [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Sättare för [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Inställare för [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Inställare för [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Inställare för [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Inställare för [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Startar automatiskt märkning av alla ytterligare ändringar du gör i dokumentet programatiskt som revisionsändringar. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Startar automatiskt märkning av alla ytterligare ändringar du gör i dokumentet programatiskt som revisionsändringar. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Stoppar automatisk märkning av dokumentändringar som revisioner. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Kopplar bort fält i hela dokumentet. |
| [Unprotect](./unprotect/)() | Tar bort skyddet från dokumentet oavsett lösenord. |
| [Unprotect](./unprotect/)(const System::String\&) | Tar bort skyddet från dokumentet om ett korrekt lösenord anges. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Uppdaterar egenskapen [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) för alla fotnoter och slutnoter i dokumentet. |
| [UpdateFields](./updatefields/)() | Uppdaterar värdena för fält i hela dokumentet. |
| [UpdateListLabels](./updatelistlabels/)() | Uppdaterar listetiketter för alla listobjekt i dokumentet. |
| [UpdatePageLayout](./updatepagelayout/)() | Bygger om sidlayouten för dokumentet. |
| [UpdateTableLayout](./updatetablelayout/)() | Implementerar ett tidigare tillvägagångssätt för omberäkning av tabellkolumnbredder som har kända problem. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Uppdaterar [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) för dokumentet enligt de angivna alternativen. |
| [UpdateThumbnail](./updatethumbnail/)() | Uppdaterar [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) för dokumentet med standardalternativ. |
| [UpdateWordCount](./updatewordcount/)() | Uppdaterar ordantalsegenskaperna för dokumentet. |
| [UpdateWordCount](./updatewordcount/)(bool) | Uppdaterar ordantalsegenskaperna för dokumentet, och uppdaterar eventuellt egenskapen [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/). |
## Anmärkningar


Det [Document](./) är ett centralt objekt i Aspose.Words-biblioteket.

För att läsa in ett befintligt dokument i något av [LoadFormat](../loadformat/) formaten, skicka ett filnamn eller en ström till en av [Document](./) konstruktorerna. För att skapa ett tomt dokument, anropa konstruktören utan parametrar.

Använd en av Save-metodens överlagringar för att spara dokumentet i något av [SaveFormat](../saveformat/) formaten.

För att rita dokumentets sidor direkt på ett **Graphics**-objekt, använd metoden [RenderToScale()](../) eller [RenderToSize()](../).

För att skriva ut dokumentet, använd en av [Print()](../) metoderna.

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

Det [Document](./) är en rotnod i ett träd som innehåller alla andra noder i dokumentet. Trädet är ett Composite-designmönster och liknar på många sätt XmlDocument. Innehållet i dokumentet kan manipuleras fritt programatiskt:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Överväg att använda [DocumentBuilder](../documentbuilder/) som förenklar uppgiften att programatiskt skapa eller fylla i dokumentträdet.

Det [Document](./) kan bara innehålla [Section](../section/) objekt.

I Microsoft Word måste ett giltigt dokument ha minst en sektion.
## Se även

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
