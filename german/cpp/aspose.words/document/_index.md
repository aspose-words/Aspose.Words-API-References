---
title: "Aspose::Words::Document class"
linktitle: "Dokument"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document class. Stellt ein Word‑Dokument dar. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words/document/
---
## Document class


Stellt ein Word-Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Akzeptiert alle nachverfolgten Änderungen im Dokument. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende des Dokuments zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Anfang des Dokuments zu besuchen. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Fügt das angegebene Dokument am Ende dieses Dokuments an. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Fügt das angegebene Dokument am Ende dieses Dokuments an. |
| [Cleanup](./cleanup/)() | Bereinigt ungenutzte Formatvorlagen und Listen aus dem Dokument. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Bereinigt ungenutzte Formatvorlagen und Listen aus dem Dokument, abhängig von den angegebenen [CleanupOptions](../cleanupoptions/). |
| [Clone](./clone/)() | Führt eine tiefe Kopie des [Document](./) durch. |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Vergleicht dieses Dokument mit einem anderen Dokument und erzeugt Änderungen als Anzahl von Bearbeitungs‑ und Formatierungsrevisionen [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Vergleicht dieses Dokument mit einem anderen Dokument und erzeugt Änderungen als Anzahl von Bearbeitungs‑ und Formatierungsrevisionen [Revision](../revision/). Ermöglicht die Angabe von Vergleichsoptionen mittels [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Kopiert Formatvorlagen von der angegebenen Vorlage in ein Dokument. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Kopiert Formatvorlagen von der angegebenen Vorlage in ein Dokument. |
| [Document](./document/)() | Erstellt ein leeres Word‑Dokument. |
| [Document](./document/)(const System::String\&) | Öffnet ein vorhandenes Dokument aus einer Datei. Erkennt das Dateiformat automatisch. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Öffnet ein vorhandenes Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie ein Verschlüsselungspasswort. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Öffnet ein vorhandenes Dokument aus einem Stream. Erkennt das Dateiformat automatisch. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Öffnet ein vorhandenes Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie ein Verschlüsselungspasswort. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Konvertiert in Tabellenstilen angegebene Formatierungen in direkte Formatierungen von Tabellen im Dokument. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Gibt das [Document](./)-Objekt zurück, das den angegebenen Seitenbereich und die angegebenen Extraktionsoptionen für Seiten darstellt. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Gibt das [Document](./)-Objekt zurück, das den angegebenen Seitenbereich darstellt. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Liest oder legt den vollständigen Pfad der dem Dokument angehängten Vorlage fest. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Liest oder legt ein Flag fest, das angibt, ob die Formatvorlagen im Dokument jedes Mal, wenn das Dokument in MS Word geöffnet wird, an die Formatvorlagen der angehängten Vorlage angepasst werden. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Liest oder legt die Hintergrundform des Dokuments fest. Kann **null** sein. |
| [get_Bibliography](./get_bibliography/)() | Liest das [Bibliography](./get_bibliography/)-Objekt, das die Liste der im Dokument verfügbaren Quellen darstellt. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments repräsentiert. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Bietet Zugriff auf Dokumentkompatibilitätsoptionen (d. h. die Benutzereinstellungen, die auf der **Compatibility**-Registerkarte des **Options**-Dialogs in Word eingegeben wurden). |
| [get_Compliance](./get_compliance/)() | Liest die OOXML‑Konformitätsversion, die aus dem geladenen Dokumentinhalt ermittelt wird. Sinnvoll nur für OOXML‑Dokumente. |
| [get_Count](../compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Gibt eine Sammlung zurück, die alle benutzerdefinierten Dokumenteigenschaften des Dokuments repräsentiert. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Liest oder legt die Sammlung der Custom XML Data Storage Parts fest. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Liest oder legt das Intervall (in Punkten) zwischen den Standard-Tabulatoren fest. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Liest die Sammlung digitaler Signaturen für dieses Dokument und deren Validierungsergebnisse. |
| [get_Document](../documentbase/get_document/)() const override | Liest diese Instanz. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Bietet Optionen, die die Nummerierung und Positionierung von Endnoten in diesem Dokument steuern. |
| [get_FieldOptions](./get_fieldoptions/)() | Liest ein [FieldOptions](../../aspose.words.fields/fieldoptions/)-Objekt, das Optionen zur Steuerung der Feldverarbeitung im Dokument darstellt. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FirstSection](./get_firstsection/)() | Liest den ersten Abschnitt im Dokument. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten. |
| [get_FontSettings](./get_fontsettings/)() const | Liest oder legt die Schriftarteinstellungen des Dokuments fest. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Bietet Optionen, die die Nummerierung und Positionierung von Fußnoten in diesem Dokument steuern. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Bietet Zugriff auf die im Dokument definierten Fußnoten-/Endnoten‑Trennzeichen. |
| [get_Frameset](./get_frameset/)() const | Gibt eine [Frameset](./get_frameset/)-Instanz zurück, wenn dieses Dokument eine Frames‑Seite darstellt. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Liest oder legt das Glossar-Dokument innerhalb dieses Dokuments oder dieser Vorlage fest. Ein Glossar-Dokument ist ein Speicher für AutoText-, AutoCorrect- und Building‑Block‑Einträge, die in einem Dokument definiert sind. |
| [get_GrammarChecked](./get_grammarchecked/)() | Gibt **true** zurück, wenn das Dokument auf Grammatik geprüft wurde. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_HasMacros](./get_hasmacros/)() | Gibt **true** zurück, wenn das Dokument ein VBA‑Projekt (Makros) enthält. |
| [get_HasRevisions](./get_hasrevisions/)() | Gibt **true** zurück, wenn das Dokument Änderungen nachverfolgt hat. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Bietet Zugriff auf Optionen für die Silbentrennung von Dokumenten. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzählstatistik einbezogen werden sollen. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_JustificationMode](./get_justificationmode/)() | Liest oder legt die Zeichenabstandsanpassung eines Dokuments fest. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_LastSection](./get_lastsection/)() | Liest den letzten Abschnitt im Dokument. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Liest ein [LayoutOptions](../../aspose.words.layout/layoutoptions/) Objekt, das Optionen zur Steuerung des Layoutprozesses dieses Dokuments darstellt. |
| [get_Lists](../documentbase/get_lists/)() const | Stellt Zugriff auf die im Dokument verwendete Listformatierung bereit. |
| [get_MailMerge](./get_mailmerge/)() | Gibt ein [MailMerge](../../aspose.words.mailmerging/mailmerge/) Objekt zurück, das die Seriendruckfunktionalität für das Dokument darstellt. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Liest oder legt das Objekt fest, das alle Seriendruckinformationen für ein Dokument enthält. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [Document](../nodetype/) zurück. |
| [get_OriginalFileName](./get_originalfilename/)() const | Liest den ursprünglichen Dateinamen des Dokuments. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Liest das Format des ursprünglichen Dokuments, das in dieses Objekt geladen wurde. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Liest oder legt die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) fest, die über \"unknown relationships\" mit dem OOXML-Paket verknüpft sind. |
| [get_PageColor](../documentbase/get_pagecolor/)() | Liest oder legt die Seitenfarbe des Dokuments fest. Diese Eigenschaft ist eine vereinfachte Version von [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | Liest die Anzahl der Seiten im Dokument, wie sie durch die zuletzt durchgeführte Seitenlayout-Operation berechnet wurde. |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Liest den aktuell aktiven Dokumentenschutztyp. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Gibt an, ob Kerning sowohl auf lateinischen Text als auch auf Interpunktion angewendet wird. |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Stellt Informationen zum Lesbarkeitswert des Dokuments bereit. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Liest oder legt ein Flag fest, das angibt, dass Microsoft Word beim Speichern des Dokuments alle Benutzerinformationen aus Kommentaren, Änderungen und Dokumenteigenschaften entfernt. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [get_Revisions](./get_revisions/)() | Liest eine Sammlung von Revisionen (nachverfolgte Änderungen), die in diesem Dokument existieren. |
| [get_RevisionsView](./get_revisionsview/)() const | Liest oder legt einen Wert fest, der angibt, ob mit der Original- oder der überarbeiteten Version eines Dokuments gearbeitet werden soll. |
| [get_Sections](./get_sections/)() | Gibt eine Sammlung zurück, die alle Abschnitte im Dokument darstellt. |
| [get_ShadeFormData](./get_shadeformdata/)() | Gibt an, ob die graue Schattierung bei Formularfeldern aktiviert werden soll. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Gibt an, ob Grammatikfehler in diesem Dokument angezeigt werden sollen. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Gibt an, ob Rechtschreibfehler in diesem Dokument angezeigt werden sollen. |
| [get_SpellingChecked](./get_spellingchecked/)() | Gibt **true** zurück, wenn das Dokument auf Rechtschreibung geprüft wurde. |
| [get_Styles](../documentbase/get_styles/)() const | Gibt eine Sammlung von im Dokument definierten Stilen zurück. |
| [get_Theme](./get_theme/)() | Liest das [Theme](./get_theme/)‑Objekt für dieses Dokument. |
| [get_TrackRevisions](./get_trackrevisions/)() | True, wenn Änderungen nachverfolgt werden, wenn dieses Dokument in Microsoft Word bearbeitet wird. |
| [get_Variables](./get_variables/)() | Gibt die Sammlung von Variablen zurück, die zu einem Dokument oder einer Vorlage hinzugefügt wurden. |
| [get_VbaProject](./get_vbaproject/)() const | Liest oder setzt ein [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Liest die Anzahl der Dokumentversionen, die im DOC‑Dokument gespeichert wurden. |
| [get_ViewOptions](./get_viewoptions/)() | Bietet Optionen, um zu steuern, wie das Dokument in Microsoft Word angezeigt wird. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Wird während verschiedener Dokumentverarbeitungsabläufe aufgerufen, wenn ein Problem erkannt wird, das zu Daten‑ oder Formatierungsverlust führen könnte. |
| [get_Watermark](./get_watermark/)() | Stellt Zugriff auf das Dokumentwasserzeichen bereit. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Gibt eine Sammlung zurück, die eine Liste von Task‑Pane‑Add‑Ins darstellt. |
| [get_WriteProtection](./get_writeprotection/)() | Stellt Zugriff auf die Schreibschutzoptionen des Dokuments bereit. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Liest die Seitengröße, Ausrichtung und weitere Informationen über eine Seite, die für den Druck oder das Rendern nützlich sein können. |
| [GetText](../compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Führt Läufe mit gleicher Formatierung in allen Absätzen des Dokuments zusammen. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Ändert Feldtypwerte [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) von [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) im gesamten Dokument, sodass sie den in den Feldcodes enthaltenen Feldtypen entsprechen. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Schützt das Dokument vor Änderungen, ohne das vorhandene Passwort zu ändern, oder weist ein zufälliges Passwort zu. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Schützt das Dokument vor Änderungen und legt optional ein Schutzpasswort fest. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveBlankPages](./removeblankpages/)() | Entfernt leere Seiten aus dem Dokument. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Entfernt Toolbar‑ und Tastaturbefehlsanpassungen aus dem Dokument. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Entfernt externe XML‑Schemainreferenzen aus diesem Dokument. |
| [RemoveMacros](./removemacros/)() | Entfernt alle Makros (das VBA‑Projekt) sowie Toolbars und Befehlsanpassungen aus dem Dokument. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Rendert eine Dokumentseite in ein **Graphics**‑Objekt mit einem angegebenen Maßstab. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Rendert eine Dokumentseite in ein **Graphics**-Objekt mit einer angegebenen Größe. |
| [Save](./save/)(const System::String\&) | Speichert das Dokument in einer Datei. Bestimmt das Speicherformat automatisch anhand der Erweiterung. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Speichert das Dokument in einer Datei im angegebenen Format. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Speichert das Dokument in einer Datei unter Verwendung der angegebenen Speicheroptionen. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Speichert das Dokument in einen Stream unter Verwendung des angegebenen Formats. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Speichert das Dokument in einen Stream unter Verwendung der angegebenen Speicheroptionen. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Wählt den ersten [Node](../node/) aus, der dem XPath‑Ausdruck entspricht. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Setter für [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Setter für [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Setter für [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Setter für [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Setter für [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter für [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Setter für [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Setter für [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Setter für [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Setter für [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Setter für [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Setter für [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Setter für [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Setter für [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Setter für [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Setter für [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Setter für [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Setter für [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Setter für [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Setter für [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Setter für [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Setter für [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter für [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Stoppt die automatische Markierung von Dokumentänderungen als Revisionen. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Entkoppelt Felder im gesamten Dokument. |
| [Unprotect](./unprotect/)() | Entfernt den Schutz des Dokuments, unabhängig vom Passwort. |
| [Unprotect](./unprotect/)(const System::String\&) | Entfernt den Schutz des Dokuments, wenn ein korrektes Passwort angegeben wird. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Aktualisiert die [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) Eigenschaft aller Fußnoten und Endnoten im Dokument. |
| [UpdateFields](./updatefields/)() | Aktualisiert die Werte der Felder im gesamten Dokument. |
| [UpdateListLabels](./updatelistlabels/)() | Aktualisiert die Listeneinträge für alle Listenelemente im Dokument. |
| [UpdatePageLayout](./updatepagelayout/)() | Erstellt das Seitenlayout des Dokuments neu. |
| [UpdateTableLayout](./updatetablelayout/)() | Implementiert einen früheren Ansatz zur Neuberechnung von Tabellenspaltenbreiten, der bekannte Probleme hat. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Aktualisiert das [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) des Dokuments gemäß den angegebenen Optionen. |
| [UpdateThumbnail](./updatethumbnail/)() | Aktualisiert das [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) des Dokuments mit den Standardoptionen. |
| [UpdateWordCount](./updatewordcount/)() | Aktualisiert die Wortzählungs-Eigenschaften des Dokuments. |
| [UpdateWordCount](./updatewordcount/)(bool) | Aktualisiert die Wortzählungs-Eigenschaften des Dokuments, optional wird die [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/) Eigenschaft aktualisiert. |
## Hinweise


Das [Document](./) ist ein zentrales Objekt in der Aspose.Words-Bibliothek.

Um ein vorhandenes Dokument in einem der [LoadFormat](../loadformat/) Formate zu laden, übergeben Sie einen Dateinamen oder einen Stream an einen der [Document](./) Konstruktoren. Um ein leeres Dokument zu erstellen, rufen Sie den Konstruktor ohne Parameter auf.

Verwenden Sie eine der Überladungen der Save-Methode, um das Dokument in einem der [SaveFormat](../saveformat/) Formate zu speichern.

Um Dokumentseiten direkt auf ein **Graphics**-Objekt zu zeichnen, verwenden Sie die Methode [RenderToScale()](../) oder [RenderToSize()](../).

Um das Dokument zu drucken, verwenden Sie eine der [Print()](../) Methoden.

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

Das [Document](./) ist ein Wurzelknoten eines Baums, der alle anderen Knoten des Dokuments enthält. Der Baum ist ein Composite-Entwurfsmuster und in vielerlei Hinsicht dem XmlDocument ähnlich. Der Inhalt des Dokuments kann programmgesteuert frei manipuliert werden:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Erwägen Sie die Verwendung von [DocumentBuilder](../documentbuilder/), der die Aufgabe vereinfacht, den Dokumentbaum programmgesteuert zu erstellen oder zu füllen.

Das [Document](./) kann nur [Section](../section/) Objekte enthalten.

In Microsoft Word muss ein gültiges Dokument mindestens einen Abschnitt enthalten.
## Siehe auch

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
