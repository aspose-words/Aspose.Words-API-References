---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Document-Klasse für die nahtlose Bearbeitung von Word-Dokumenten. Optimieren Sie Ihre Projekte mit leistungsstarken Funktionen und einfacher Integration.
type: docs
weight: 640
url: /de/net/aspose.words/document/
---
## Document class

Stellt ein Word-Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Dokumenten](https://docs.aspose.com/words/net/working-with-document/) Dokumentationsartikel.

```csharp
public class Document : DocumentBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Document](document/#constructor)() | Erstellt ein leeres Word-Dokument. |
| [Document](document/#constructor_1)(*Stream*) | Öffnet ein vorhandenes Dokument aus einem Stream. Das Dateiformat wird automatisch erkannt. |
| [Document](document/#constructor_3)(*string*) | Öffnet ein vorhandenes Dokument aus einer Datei. Das Dateiformat wird automatisch erkannt. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Öffnet ein vorhandenes Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen, wie z. B. eines Verschlüsselungskennworts. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Öffnet ein vorhandenes Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt ihn fest. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Ruft ein Flag ab oder legt ein Flag fest, das angibt, ob die Stile im Dokument bei jedem Öffnen des Dokuments in MS Word aktualisiert werden, um mit den Stilen in der angehängten Vorlage übereinzustimmen. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Ruft die Hintergrundform des Dokuments ab oder legt sie fest. Kann sein`null` . |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | Ruft die[`Bibliography`](./bibliography/)Objekt, das die Liste der im Dokument verfügbaren Quellen darstellt. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments darstellt. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Bietet Zugriff auf Dokumentkompatibilitätsoptionen (d. h. die Benutzereinstellungen, die auf dem**Kompatibilität** Registerkarte des**Optionen**Dialogfeld in Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Ruft die OOXML-Konformitätsversion ab, die aus dem geladenen Dokumentinhalt ermittelt wurde. Ist nur für OOXML-Dokumente sinnvoll. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Gibt eine Sammlung zurück, die alle benutzerdefinierten Dokumenteigenschaften des Dokuments darstellt. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Ruft die Auflistung der benutzerdefinierten XML-Datenspeicherteile ab oder legt sie fest. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Ruft das Intervall (in Punkten) zwischen den Standard-Tabstopps ab oder legt es fest. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Ruft die Sammlung digitaler Signaturen für dieses Dokument und deren Validierungsergebnisse ab. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Ruft diese Instanz ab. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Endnoten in diesem Dokument. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Erhält eine[`FieldOptions`](../../aspose.words.fields/fieldoptions/) Objekt, das Optionen zur Steuerung der Feldbehandlung im Dokument darstellt. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Ruft den ersten Abschnitt im Dokument ab. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Ruft die Schriftarteinstellungen des Dokuments ab oder legt sie fest. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Fußnoten in diesem Dokument. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Bietet Zugriff auf die im Dokument definierten Fußnoten-/Endnotentrennzeichen. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Gibt einen[`Frameset`](./frameset/) Instanz, wenn dieses Dokument eine Frames-Seite darstellt. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Ruft das Glossardokument innerhalb dieses Dokuments oder dieser Vorlage ab oder legt es fest. Ein Glossardokument ist ein Speicher für in einem Dokument definierte AutoText-, AutoKorrektur- und Bausteineinträge. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Rückgaben`WAHR` ob das Dokument auf Grammatik geprüft wurde. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Rückgaben`WAHR` wenn das Dokument ein VBA-Projekt (Makros) enthält. |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Rückgaben`WAHR` ob das Dokument nachverfolgte Änderungen enthält. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Bietet Zugriff auf Dokument-Silbentrennungsoptionen. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzählstatistik einbezogen werden sollen. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Ruft die Zeichenabstandsanpassung eines Dokuments ab oder legt diese fest. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Ruft den letzten Abschnitt im Dokument ab. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Erhält eine[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) Objekt, das Optionen zur Steuerung des Layoutprozesses dieses Dokuments darstellt. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Bietet Zugriff auf die im Dokument verwendete Listenformatierung. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Gibt einen[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) Objekt, das die Serienbrieffunktion für das Dokument darstellt. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Ruft das Objekt ab oder legt es fest, das alle Seriendruckinformationen für ein Dokument enthält. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder daraus entfernt wird. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | RückgabenDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Ruft den ursprünglichen Dateinamen des Dokuments ab. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Ruft das Format des Originaldokuments ab, das in dieses Objekt geladen wurde. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Ruft die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) ab oder legt sie fest, die über „unbekannte Beziehungen“ mit dem OOXML-Paket verknüpft sind. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Ruft die Seitenfarbe des Dokuments ab oder legt sie fest. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Ruft die Anzahl der Seiten im Dokument ab, die durch den letzten Seitenlayoutvorgang berechnet wurde. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Ruft den aktuell aktiven Dokumentschutztyp ab. |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | Gibt an, ob das Kerning sowohl auf lateinischen Text als auch auf die Zeichensetzung angewendet wird. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, dass Microsoft Word beim Speichern des Dokuments alle Benutzerinformationen aus Kommentaren, Revisionen und Dokumenteigenschaften entfernt. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung des Ladens externer Ressourcen. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Ruft eine Sammlung von Revisionen (nachverfolgten Änderungen) ab, die in diesem Dokument vorhanden sind. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll. |
| [Sections](../../aspose.words/document/sections/) { get; } | Gibt eine Sammlung zurück, die alle Abschnitte im Dokument darstellt. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Gibt an, ob die graue Schattierung für Formularfelder aktiviert werden soll. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Gibt an, ob Grammatikfehler in diesem Dokument angezeigt werden sollen. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Gibt an, ob Rechtschreibfehler in diesem Dokument angezeigt werden sollen. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Rückgaben`WAHR` wenn das Dokument auf Rechtschreibung geprüft wurde. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Gibt eine Sammlung der im Dokument definierten Stile zurück. |
| [Theme](../../aspose.words/document/theme/) { get; } | Ruft die[`Theme`](./theme/) Objekt für dieses Dokument. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | „True“, wenn Änderungen nachverfolgt werden, wenn dieses Dokument in Microsoft Word bearbeitet wird. |
| [Variables](../../aspose.words/document/variables/) { get; } | Gibt die Sammlung der Variablen zurück, die einem Dokument oder einer Vorlage hinzugefügt wurden. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Ruft ab oder setzt einen[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Ruft die Anzahl der Dokumentversionen ab, die im DOC-Dokument gespeichert wurden. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Bietet Optionen zur Steuerung der Anzeige des Dokuments in Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Wird während verschiedener Dokumentverarbeitungsverfahren aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Bietet Zugriff auf das Dokumentwasserzeichen. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Gibt eine Auflistung zurück, die eine Liste von Aufgabenbereich-Add-Ins darstellt. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Bietet Zugriff auf die Schreibschutzoptionen für Dokumente. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Akzeptiert alle nachverfolgten Änderungen im Dokument. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher zum Aufrufen des Dokumentenendes. |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Dokumentanfangs. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Fügt das angegebene Dokument an das Ende dieses Dokuments an. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Fügt das angegebene Dokument an das Ende dieses Dokuments an. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Löscht nicht verwendete Stile und Listen aus dem Dokument. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Löscht nicht verwendete Stile und Listen aus dem Dokument, abhängig von der gegebenen[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Führt eine vollständige Kopie der`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Vergleicht dieses Dokument mit einem anderen Dokument und führt zu Änderungen hinsichtlich der Anzahl der Bearbeitungen und Formatänderungen.[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht dieses Dokument mit einem anderen Dokument und führt zu Änderungen in Form von Bearbeitungs- und Formatänderungen.[`Revision`](../revision/) . Ermöglicht die Angabe von Vergleichsoptionen mit[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Kopiert Stile aus der angegebenen Vorlage in ein Dokument. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Kopiert Stile aus der angegebenen Vorlage in ein Dokument. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Wandelt die in Tabellenstilen angegebene Formatierung in direkte Formatierung der Tabellen im Dokument um. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | Gibt die`Document` Objekt, das den angegebenen Seitenbereich darstellt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Ruft die Seitengröße, Ausrichtung und andere Informationen zu einer Seite ab, die zum Drucken oder Rendern nützlich sein können. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Verknüpfungen werden mit der gleichen Formatierung in allen Absätzen des Dokuments ausgeführt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Ändert Feldtypwerte[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) im gesamten Dokument, sodass sie den in den Feldfunktionen enthaltenen Feldtypen entsprechen. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Print](../../aspose.words/document/print/#print)() | Druckt das gesamte Dokument auf dem Standarddrucker. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Druckt das Dokument gemäß den angegebenen Druckereinstellungen unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche). |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Drucken Sie das gesamte Dokument auf dem angegebenen Drucker, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche). |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Druckt das Dokument entsprechend den angegebenen Druckereinstellungen, unter Verwendung des Standard-Druckcontrollers (ohne Benutzeroberfläche) und eines Dokumentnamens. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Schützt das Dokument vor Änderungen, ohne das bestehende Passwort zu ändern oder vergibt ein zufälliges Passwort. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Schützt das Dokument vor Änderungen und legt optional ein Schutzkennwort fest. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | Entfernt leere Seiten aus dem Dokument. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Entfernt externe XML-Schemareferenzen aus diesem Dokument. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Entfernt alle Makros (das VBA-Projekt) sowie Symbolleisten und Befehlsanpassungen aus dem Dokument. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Rendert eine Dokumentseite in eineGraphics Objekt auf einen bestimmten Maßstab. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Rendert eine Dokumentseite in eineGraphics Objekt auf eine angegebene Größe. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Speichert das Dokument in einer Datei. Das Speicherformat wird automatisch anhand der Erweiterung ermittelt. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Speichert das Dokument im angegebenen Format in einem Stream. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Speichert das Dokument unter Verwendung der angegebenen Speicheroptionen in einem Stream. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Speichert das Dokument in einer Datei im angegebenen Format. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Speichert das Dokument mit den angegebenen Speicheroptionen in einer Datei. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Sendet das Dokument an den Client-Browser. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../node/) das dem XPath-Ausdruck entspricht. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Beginnt automatisch, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Stoppt die automatische Kennzeichnung von Dokumentänderungen als Revisionen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Hebt die Verknüpfung von Feldern im gesamten Dokument auf. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Entfernt den Schutz des Dokuments, unabhängig vom Kennwort. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Entfernt den Schutz vom Dokument, wenn ein korrektes Kennwort angegeben ist. |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | Aktualisiert die[`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/) Eigenschaft aller Fußnoten und Endnoten im Dokument. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Aktualisiert die Werte der Felder im gesamten Dokument. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Aktualisiert Listenbeschriftungen für alle Listenelemente im Dokument. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Erstellt das Seitenlayout des Dokuments neu. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Aktualisierungen[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments mit Standardoptionen. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Aktualisierungen[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments gemäß den angegebenen Optionen. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Aktualisiert die Wortanzahleigenschaften des Dokuments. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Aktualisiert die Wortanzahleigenschaften des Dokuments, aktualisiert optional[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) Eigenschaft. |

## Bemerkungen

Der`Document` ist ein zentrales Objekt in der Aspose.Words-Bibliothek.

Um ein vorhandenes Dokument in einem der[`LoadFormat`](../loadformat/) Formate, übergeben Sie einen Dateinamen oder einen Stream in eines der`Document` Konstruktoren. Um ein leeres Dokument zu erstellen, rufen Sie den Konstruktor ohne Parameter auf.

Verwenden Sie eine der Save-Methodenüberladungen, um das Dokument in einem der [`SaveFormat`](../saveformat/) Formate.

Um Dokumentseiten direkt auf ein**Grafik** Objekt use [`RenderToScale`](./rendertoscale/) oder[`RenderToSize`](./rendertosize/) Verfahren.

Um das Dokument auszudrucken, verwenden Sie eine der[`Print`](./print/) Methoden.

[`MailMerge`](./mailmerge/)ist die Berichts-Engine von Aspose.Words, mit der sich in Microsoft Word erstellte Berichte schnell und einfach mit Daten aus verschiedenen Datenquellen füllen lassen. Die Daten können aus einem DataSet, einer DataTable, einer DataView, einem IDataReader oder einem Werte-Array stammen.**Serienbrief** geht die in der Datenquelle gefundenen Datensätze durch und fügt sie in Serienbrieffelder im Dokument ein und erweitert es nach Bedarf.

`Document` speichert dokumentenweite Informationen wie[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) , Listen und Makros. Die meisten dieser Objekte sind über die entsprechenden Eigenschaften des`Document`.

Der`Document` ist ein Stammknoten eines Baums, der alle anderen Knoten des Dokuments enthält. Der Baum ist ein Composite-Entwurfsmuster und ähnelt in vielerlei Hinsicht XmlDocument. Der Inhalt des Dokuments kann programmgesteuert frei bearbeitet werden:

* Auf die Knoten des Dokuments kann über typisierte Sammlungen zugegriffen werden, beispielsweise[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) usw.
* Die Knoten des Dokuments können nach ihrem Knotentyp ausgewählt werden mit [`GetChildNodes`](../compositenode/getchildnodes/) oder mithilfe einer XPath-Abfrage mit[`SelectNodes`](../compositenode/selectnodes/) oder[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Inhaltsknoten können überall im Dokument hinzugefügt oder entfernt werden, indem [`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) und andere -Methoden, die von der Basisklasse bereitgestellt werden[`CompositeNode`](../compositenode/).
* Die Formatierungsattribute jedes Knotens können über die Eigenschaften dieses Knotens geändert werden.

Erwägen Sie die Verwendung[`DocumentBuilder`](../documentbuilder/) Dies vereinfacht die Aufgabe, programmgesteuert x000d_ zu erstellen oder den Dokumentbaum aufzufüllen.

Der`Document` kann nur enthalten[`Section`](../section/) Objekte.

In Microsoft Word muss ein gültiges Dokument mindestens einen Abschnitt enthalten.

## Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nachfolgend finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Serienbrief zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um für jede Zeile in der Tabelle ein Ausgabe-Seriendruckdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Serienbrief-Ausgabedokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Serienbrief-Quelldokument.
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

### Siehe auch

* class [DocumentBase](../documentbase/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
