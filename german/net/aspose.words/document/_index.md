---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Aspose.Words.Document klas. Stellt ein WordDokument dar in C#.
type: docs
weight: 430
url: /de/net/aspose.words/document/
---
## Document class

Stellt ein Word-Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Dokument](https://docs.aspose.com/words/net/working-with-document/) Dokumentationsartikel.

```csharp
public class Document : DocumentBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Document](document/#constructor)() | Erstellt ein leeres Word-Dokument. |
| [Document](document/#constructor_1)(*Stream*) | Öffnet ein vorhandenes Dokument aus einem Stream. Erkennt automatisch das Dateiformat. |
| [Document](document/#constructor_3)(*string*) | Öffnet ein vorhandenes Dokument aus einer Datei. Erkennt automatisch das Dateiformat. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Öffnet ein vorhandenes Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Öffnet ein vorhandenes Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt diesen fest. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob die Stile im Dokument bei jedem Öffnen des Dokuments in MS Word so aktualisiert werden, dass sie mit den Stilen in der angehängten Vorlage übereinstimmen. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Ruft die Hintergrundform des Dokuments ab oder legt diese fest. Kann sein`Null` . |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments darstellt. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Bietet Zugriff auf Dokumentkompatibilitätsoptionen (d. h. die Benutzereinstellungen, die im eingegeben wurden).**Kompatibilität** Registerkarte des**Optionen** Dialog in Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Ruft die aus dem geladenen Dokumentinhalt ermittelte OOXML-Konformitätsversion ab. Ist nur für OOXML-Dokumente sinnvoll. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Gibt eine Sammlung zurück, die alle benutzerdefinierten Dokumenteigenschaften des Dokuments darstellt. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Ruft die Sammlung benutzerdefinierter XML-Datenspeicherteile ab oder legt diese fest. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Ruft das Intervall (in Punkt) zwischen den Standardtabstopps ab oder legt es fest. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Ruft die Sammlung digitaler Signaturen für dieses Dokument und deren Validierungsergebnisse ab. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Ruft diese Instanz ab. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Bietet Optionen, die die Nummerierung und Positionierung von Endnoten in diesem Dokument steuern. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Ruft a ab[`FieldOptions`](../../aspose.words.fields/fieldoptions/) Objekt, das Optionen zur Steuerung der Feldverarbeitung im Dokument darstellt. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Ruft den ersten Abschnitt im Dokument ab. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Ruft Einstellungen für Dokumentschriftarten ab oder legt diese fest. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Bietet Optionen, die die Nummerierung und Positionierung von Fußnoten in diesem Dokument steuern. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Gibt a zurück[`Frameset`](./frameset/)Beispiel, wenn dieses Dokument eine Frames-Seite darstellt. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Ruft das Glossardokument in diesem Dokument oder dieser Vorlage ab oder legt es fest. Ein Glossardokument ist ein Speicher für AutoText-, AutoCorrect- und Building Block-Einträge, die in einem Dokument definiert sind. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Gibt zurück`WAHR` wenn das Dokument auf Grammatik überprüft wurde. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Gibt zurück`WAHR` wenn das Dokument ein VBA-Projekt (Makros) hat. |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Gibt zurück`WAHR` ob das Dokument nachverfolgte Änderungen aufweist. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Bietet Zugriff auf Silbentrennungsoptionen für Dokumente. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Gibt an, ob Textfelder, Fußnoten und Endnoten in die Wortzahlstatistik einbezogen werden sollen. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Ruft die Zeichenabstandsanpassung eines Dokuments ab oder legt diese fest. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Ruft den letzten Abschnitt im Dokument ab. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Ruft a ab[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) Objekt, das Optionen zur Steuerung des Layoutprozesses dieses Dokuments darstellt. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Bietet Zugriff auf die im Dokument verwendete Listenformatierung. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Gibt a zurück[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) Objekt, das die Serienbrieffunktion für das Dokument darstellt. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Ruft das Objekt ab oder legt es fest, das alle Serienbriefinformationen für ein Dokument enthält. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Wird aufgerufen, wenn ein Knoten in das Dokument eingefügt oder entfernt wird. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | Gibt zurückDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Ruft den ursprünglichen Dateinamen des Dokuments ab. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Ruft das Format des Originaldokuments ab, das in dieses Objekt geladen wurde. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Ruft die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) ab oder legt diese fest, die über „unbekannte Beziehungen“ mit dem OOXML-Paket verknüpft sind. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Ruft die Seitenfarbe des Dokuments ab oder legt diese fest. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Ruft die Anzahl der Seiten im Dokument ab, wie durch den letzten Seitenlayout-Vorgang berechnet. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Ruft den aktuell aktiven Dokumentenschutztyp ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, dass Microsoft Word beim Speichern des Dokuments alle Benutzerinformationen aus Kommentaren, Überarbeitungen und Dokumenteigenschaften entfernt. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Ruft eine Sammlung von Revisionen (nachverfolgten Änderungen) ab, die in diesem Dokument vorhanden sind. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob mit der Originalversion oder der überarbeiteten Version eines Dokuments gearbeitet werden soll. |
| [Sections](../../aspose.words/document/sections/) { get; } | Gibt eine Sammlung zurück, die alle Abschnitte im Dokument darstellt. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Gibt an, ob die Grauschattierung auf Formularfeldern aktiviert werden soll. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Gibt an, ob Grammatikfehler in diesem Dokument angezeigt werden sollen. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Gibt an, ob Rechtschreibfehler in diesem Dokument angezeigt werden sollen. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Gibt zurück`WAHR` wenn das Dokument auf Rechtschreibung geprüft wurde. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Gibt eine Sammlung von im Dokument definierten Stilen zurück. |
| [Theme](../../aspose.words/document/theme/) { get; } | Ruft die ab[`Theme`](./theme/) Objekt für dieses Dokument. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | True, wenn Änderungen nachverfolgt werden, wenn dieses Dokument in Microsoft Word bearbeitet wird. |
| [Variables](../../aspose.words/document/variables/) { get; } | Gibt die Sammlung von Variablen zurück, die einem Dokument oder einer Vorlage hinzugefügt wurden. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Ruft a ab oder legt es fest[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Ruft die Anzahl der Dokumentversionen ab, die im DOC-Dokument gespeichert wurden. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Bietet Optionen zur Steuerung der Anzeige des Dokuments in Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungstreue führen könnte. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Bietet Zugriff auf das Dokumentwasserzeichen. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Gibt eine Sammlung zurück, die eine Liste von Aufgabenbereich-Add-Ins darstellt. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Bietet Zugriff auf die Schreibschutzoptionen für Dokumente. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Akzeptiert alle nachverfolgten Änderungen im Dokument. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Hängt das angegebene Dokument an das Ende dieses Dokuments an. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Hängt das angegebene Dokument an das Ende dieses Dokuments an. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Bereinigt nicht verwendete Stile und Listen aus dem Dokument. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Bereinigt je nach Angabe nicht verwendete Stile und Listen aus dem Dokument[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Führt eine tiefe Kopie des aus`Document` . |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Vergleicht dieses Dokument mit einem anderen Dokument und erzeugt Änderungen als Anzahl der Bearbeitungs- und Formatrevisionen[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Vergleicht dieses Dokument mit einem anderen Dokument und führt zu Änderungen in Form einer Reihe von Bearbeitungs- und Formatrevisionen[`Revision`](../revision/) . Ermöglicht die Angabe von Vergleichsoptionen mit[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Kopiert Stile aus der angegebenen Vorlage in ein Dokument. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Kopiert Stile aus der angegebenen Vorlage in ein Dokument. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Konvertiert die in Tabellenstilen angegebene Formatierung in direkte Formatierung für Tabellen im Dokument. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | Gibt die zurück`Document` Objekt, das den angegebenen Seitenbereich darstellt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Ruft die Seitengröße, Ausrichtung und andere Informationen zu einer Seite ab, die zum Drucken oder Rendern nützlich sein könnten. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Joins werden in allen Absätzen des Dokuments mit der gleichen Formatierung ausgeführt. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Ändert Feldtypwerte[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) im gesamten Dokument, sodass sie den in den Feldcodes enthaltenen Feldtypen entsprechen. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Print](../../aspose.words/document/print/#print)() | Druckt das gesamte Dokument auf dem Standarddrucker. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standard-Druckcontrollers (keine Benutzeroberfläche). |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Drucken Sie das gesamte Dokument auf dem angegebenen Drucker. Verwenden Sie den Standard-Druckcontroller (keine Benutzeroberfläche). |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standard-Druckcontrollers (keine Benutzeroberfläche) und eines Dokumentnamens. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Schützt das Dokument vor Änderungen, ohne das bestehende Passwort zu ändern oder weist ein zufälliges Passwort zu. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Schützt das Dokument vor Änderungen und legt optional ein Schutzpasswort fest. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Entfernt externe XML-Schema-Referenzen aus diesem Dokument. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Entfernt alle Makros (das VBA-Projekt) sowie Symbolleisten und Befehlsanpassungen aus dem Dokument. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Rendert eine Dokumentseite in eineGraphics Objekt in einem bestimmten Maßstab. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Rendert eine Dokumentseite in eineGraphics Objekt auf eine angegebene Größe. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Speichert das Dokument in einer Datei. Ermittelt automatisch das Speicherformat anhand der Erweiterung. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Speichert das Dokument im angegebenen Format in einem Stream. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Speichert das Dokument mit den angegebenen Speicheroptionen in einem Stream. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Speichert das Dokument in einer Datei im angegebenen Format. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Speichert das Dokument mit den angegebenen Speicheroptionen in einer Datei. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Sendet das Dokument an den Client-Browser. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten aus[`Node`](../node/) das entspricht dem XPath-Ausdruck. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Beginnt automatisch mit der Markierung aller weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Beginnt automatisch mit der Markierung aller weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Stoppt die automatische Markierung von Dokumentänderungen als Revisionen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Hebt die Verknüpfung von Feldern im gesamten Dokument auf. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Entfernt den Schutz vom Dokument unabhängig vom Passwort. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Entfernt den Schutz vom Dokument, wenn ein korrektes Passwort angegeben wird. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Aktualisiert die Werte von Feldern im gesamten Dokument. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Aktualisiert Listenbezeichnungen für alle Listenelemente im Dokument. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Erstellt das Seitenlayout des Dokuments neu. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Updates[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments mit Standardoptionen. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Updates[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) des Dokuments gemäß den angegebenen Optionen. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Aktualisiert die Wortanzahleigenschaften des Dokuments. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Aktualisiert die Wortanzahleigenschaften des Dokuments, optional aktualisiert[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) Eigenschaft. |

## Bemerkungen

Der`Document` ist ein zentrales Objekt in der Aspose.Words-Bibliothek.

Um ein vorhandenes Dokument in eines der zu laden[`LoadFormat`](../loadformat/) Formate, übergeben Sie einen Dateinamen oder einen Stream an eines der`Document`Konstrukteure. Um ein leeres Dokument zu erstellen, rufen Sie den Konstruktor ohne Parameter auf.

Verwenden Sie eine der Save-Methodenüberladungen, um das Dokument in einem der zu speichern.[`SaveFormat`](../saveformat/) Formate.

Um Dokumentseiten direkt auf ein zu zeichnen**Grafik** Objekt use [`RenderToScale`](./rendertoscale/) oder[`RenderToSize`](./rendertosize/) Methode.

Um das Dokument zu drucken, verwenden Sie eines der[`Print`](./print/) Methoden.

[`MailMerge`](./mailmerge/) ist die Berichts-Engine von Aspose.Words, die es ermöglicht, in Microsoft Word erstellte Berichte schnell und einfach mit Daten aus verschiedenen Datenquellen zu füllen. Die Daten können aus einem DataSet, DataTable, DataView, IDataReader oder einem Array von Werten stammen. **MailMerge** durchsucht die in der Datenquelle gefundenen Datensätze und fügt sie bei Bedarf in die Serienbrieffelder des Dokuments ein.

`Document` speichert dokumentenweite Informationen wie z[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) Listen und Makros. Auf die meisten dieser Objekte kann über die entsprechenden Eigenschaften der zugegriffen werden`Document`.

Der`Document` ist ein Wurzelknoten eines Baums, der alle anderen Knoten des Dokuments enthält. Der Baum ist ein zusammengesetztes Entwurfsmuster und ähnelt in vielerlei Hinsicht XmlDocument. Der Inhalt des Dokuments kann programmgesteuert frei manipuliert werden:

* Auf die Knoten des Dokuments kann beispielsweise über typisierte Sammlungen zugegriffen werden[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) usw.
* Die Knoten des Dokuments können anhand ihres Knotentyps mit ausgewählt werden.[`GetChildNodes`](../compositenode/getchildnodes/) oder mithilfe einer XPath-Abfrage mit[`SelectNodes`](../compositenode/selectnodes/) oder[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Inhaltsknoten können mit von überall im Dokument hinzugefügt oder entfernt werden.[`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) und other -Methoden, die von der Basisklasse bereitgestellt werden[`CompositeNode`](../compositenode/).
* Die Formatierungsattribute jedes Knotens können über die Eigenschaften dieses Knotens geändert werden.

Erwägen Sie die Verwendung[`DocumentBuilder`](../documentbuilder/)Dies vereinfacht die Aufgabe, programmgesteuert zu erstellen oder den Dokumentbaum zu füllen.

Der`Document` kann nur enthalten[`Section`](../section/) Objekte.

In Microsoft Word muss ein gültiges Dokument mindestens einen Abschnitt haben.

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
    // 1 – Verwenden Sie die gesamte Tabelle für den Serienbrief, um für jede Zeile in der Tabelle ein Ausgabe-Serienbriefdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 – Verwenden Sie eine Zeile der Tabelle, um ein Ausgabe-Serienbriefdokument zu erstellen:
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
