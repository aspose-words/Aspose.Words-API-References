---
title: Document
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt ein Word-Dokument dar.
type: docs
weight: 420
url: /de/net/aspose.words/document/
---
## Document class

Stellt ein Word-Dokument dar.

```csharp
public class Document : DocumentBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Document](document#constructor)() | Erstellt ein leeres Word-Dokument. |
| [Document](document#constructor_1)(Stream) | Öffnet ein vorhandenes Dokument aus einem Stream. Erkennt automatisch das Dateiformat. |
| [Document](document#constructor_3)(string) | Öffnet ein vorhandenes Dokument aus einer Datei. Erkennt automatisch das Dateiformat. |
| [Document](document#constructor_2)(Stream, LoadOptions) | Öffnet ein vorhandenes Dokument aus einem Stream. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |
| [Document](document#constructor_4)(string, LoadOptions) | Öffnet ein vorhandenes Dokument aus einer Datei. Ermöglicht die Angabe zusätzlicher Optionen wie z. B. eines Verschlüsselungskennworts. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate) { get; set; } | Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt ihn fest. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob die Stile im Dokument jedes Mal aktualisiert werden, damit sie mit den Stilen in der angehängten -Vorlage übereinstimmen, wenn das Dokument in MS Word geöffnet wird. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Ruft die Hintergrundform des Dokuments ab oder legt sie fest. Kann null sein. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties) { get; } | Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments darstellt. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions) { get; } | Bietet Zugriff auf Dokumentkompatibilitätsoptionen (d. h. die Benutzereinstellungen, die auf der **Kompatibilität** Registerkarte der **Optionen** Dialog in Word). |
| [Compliance](../../aspose.words/document/compliance) { get; } | Ruft die aus dem geladenen Dokumentinhalt ermittelte OOXML-Konformitätsversion ab. Nur für OOXML-Dokumente sinnvoll. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties) { get; } | Gibt eine Sammlung zurück, die alle benutzerdefinierten Dokumenteigenschaften des Dokuments darstellt. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts) { get; set; } | Ruft die Sammlung benutzerdefinierter XML-Datenspeicherteile ab oder legt sie fest. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop) { get; set; } | Ruft das Intervall (in Punkten) zwischen den Standardtabstopps ab oder legt es fest. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures) { get; } | Ruft die Sammlung digitaler Signaturen für dieses Dokument und ihre Validierungsergebnisse ab. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions) { get; } | Stellt Optionen bereit, die die Nummerierung und Positionierung von Endnoten in diesem Dokument steuern. |
| [FieldOptions](../../aspose.words/document/fieldoptions) { get; } | erhält a **Feldoptionen**Objekt, das Optionen zur Steuerung der Feldbehandlung im Dokument darstellt. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstSection](../../aspose.words/document/firstsection) { get; } | Ruft den ersten Abschnitt im Dokument ab. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Bietet Zugriff auf Eigenschaften von Schriftarten, die in diesem Dokument verwendet werden. |
| [FontSettings](../../aspose.words/document/fontsettings) { get; set; } | Ruft Schrifteinstellungen für Dokumente ab oder legt sie fest. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions) { get; } | Bietet Optionen zur Steuerung der Nummerierung und Positionierung von Fußnoten in diesem Dokument. |
| [Frameset](../../aspose.words/document/frameset) { get; } | Gibt a zurück[`Frameset`](./frameset)Instanz, wenn dieses Dokument eine Frames-Seite darstellt. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument) { get; set; } | Ruft das Glossardokument innerhalb dieses Dokuments oder dieser Vorlage ab oder legt es fest. Ein Glossardokument ist ein Speicher für AutoText-, AutoKorrektur- und Bausteineinträge, die in einem Dokument definiert sind. |
| [GrammarChecked](../../aspose.words/document/grammarchecked) { get; set; } | gibt zurück **Stimmt** wenn das Dokument auf Grammatik geprüft wurde. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [HasMacros](../../aspose.words/document/hasmacros) { get; } | gibt zurück **Stimmt** wenn das Dokument ein VBA-Projekt (Makros) hat. |
| [HasRevisions](../../aspose.words/document/hasrevisions) { get; } | gibt zurück **Stimmt** ob das Dokument nachverfolgte Änderungen aufweist. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions) { get; } | Bietet Zugriff auf Silbentrennungsoptionen für Dokumente. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastSection](../../aspose.words/document/lastsection) { get; } | Ruft den letzten Abschnitt im Dokument ab. |
| [LayoutOptions](../../aspose.words/document/layoutoptions) { get; } | erhält a **LayoutOptionen** Objekt, das Optionen zur Steuerung des Layoutprozesses dieses Dokuments darstellt. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Bietet Zugriff auf die im Dokument verwendete Listenformatierung. |
| [MailMerge](../../aspose.words/document/mailmerge) { get; } | Gibt a zurück **Seriendruck** Objekt, das die Seriendruckfunktion für das Dokument darstellt. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings) { get; set; } | Ruft das Objekt ab oder legt es fest, das alle Seriendruckinformationen für ein Dokument enthält. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| override [NodeType](../../aspose.words/document/nodetype) { get; } | gibt zurück **Knotentyp.Dokument** . |
| [OriginalFileName](../../aspose.words/document/originalfilename) { get; } | Ruft den ursprünglichen Dateinamen des Dokuments ab. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat) { get; } | Ruft das Format des Originaldokuments ab, das in dieses Objekt geladen wurde. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts) { get; set; } | Ruft die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) ab oder legt sie fest, die über "unbekannte Beziehungen" mit dem OOXML-Paket verknüpft sind. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Holt oder setzt die Seitenfarbe des Dokuments. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](../documentbase/backgroundshape) . |
| [PageCount](../../aspose.words/document/pagecount) { get; } | Ruft die Anzahl der Seiten im Dokument ab, wie durch die letzte Seitenlayoutoperation berechnet. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [ProtectionType](../../aspose.words/document/protectiontype) { get; } | Ruft den aktuell aktiven Dokumentenschutztyp ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, dass Microsoft Word beim Speichern des Dokuments alle Benutzerinformationen aus Kommentaren, Überarbeitungen und Dokumenteigenschaften entfernt. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [Revisions](../../aspose.words/document/revisions) { get; } | Ruft eine Sammlung von Revisionen (verfolgten Änderungen) ab, die in diesem Dokument vorhanden sind. |
| [RevisionsView](../../aspose.words/document/revisionsview) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob mit der ursprünglichen oder der überarbeiteten Version eines Dokuments gearbeitet werden soll. |
| [Sections](../../aspose.words/document/sections) { get; } | Gibt eine Sammlung zurück, die alle Abschnitte im Dokument darstellt. |
| [ShadeFormData](../../aspose.words/document/shadeformdata) { get; set; } | Gibt an, ob die Grauschattierung von Formularfeldern aktiviert werden soll. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors) { get; set; } | Gibt an, ob Grammatikfehler in diesem Dokument angezeigt werden sollen. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors) { get; set; } | Gibt an, ob Rechtschreibfehler in diesem Dokument angezeigt werden sollen. |
| [SpellingChecked](../../aspose.words/document/spellingchecked) { get; set; } | gibt zurück **Stimmt** wenn das Dokument auf Rechtschreibung geprüft wurde. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Gibt eine Sammlung von Stilen zurück, die im Dokument definiert sind. |
| [Theme](../../aspose.words/document/theme) { get; } | Ruft die ab[`Theme`](./theme) Objekt für dieses Dokument. |
| [TrackRevisions](../../aspose.words/document/trackrevisions) { get; set; } | **WAHR** wenn Änderungen nachverfolgt werden, wenn dieses Dokument in Microsoft Word bearbeitet wird. |
| [Variables](../../aspose.words/document/variables) { get; } | Gibt die Sammlung von Variablen zurück, die einem Dokument oder einer Vorlage hinzugefügt wurden. |
| [VbaProject](../../aspose.words/document/vbaproject) { get; set; } | Holt oder setzt a[`VbaProject`](./vbaproject) . |
| [VersionsCount](../../aspose.words/document/versionscount) { get; } | Ruft die Anzahl der Dokumentversionen ab, die im DOC-Dokument gespeichert wurde. |
| [ViewOptions](../../aspose.words/document/viewoptions) { get; } | Bietet Optionen zum Steuern der Anzeige des Dokuments in Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten oder der Formatierung führen kann. |
| [Watermark](../../aspose.words/document/watermark) { get; } | Bietet Zugriff auf das Wasserzeichen des Dokuments. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes) { get; } | Gibt eine Sammlung zurück, die eine Liste von Aufgabenbereich-Add-Ins darstellt. |
| [WriteProtection](../../aspose.words/document/writeprotection) { get; } | Bietet Zugriff auf die Schreibschutzoptionen für Dokumente. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/document/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions)() | Akzeptiert alle nachverfolgten Änderungen im Dokument. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument)(Document, ImportFormatMode) | Hängt das angegebene Dokument an das Ende dieses Dokuments an. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Hängt das angegebene Dokument an das Ende dieses Dokuments an. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup)() | Entfernt ungenutzte Stile und Listen aus dem Dokument. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup_1)(CleanupOptions) | Entfernt ungenutzte Stile und Listen je nach Vorgabe aus dem Dokument[`CleanupOptions`](../cleanupoptions) . |
| [Clone](../../aspose.words/document/clone#clone)() | Führt eine tiefe Kopie der[`Document`](../document) . |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [Compare](../../aspose.words/document/compare#compare)(Document, string, DateTime) | Vergleicht dieses Dokument mit einem anderen Dokument, das Änderungen als Anzahl der Bearbeitungs- und Formatrevisionen erzeugt[`Revision`](../revision) . |
| [Compare](../../aspose.words/document/compare#compare_1)(Document, string, DateTime, CompareOptions) | Vergleicht dieses Dokument mit einem anderen Dokument, das Änderungen als eine Reihe von Bearbeitungs- und Formatrevisionen hervorbringt[`Revision`](../revision) . Ermöglicht die Angabe von Vergleichsoptionen mit[`CompareOptions`](../../aspose.words.comparing/compareoptions) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate)(Document) | Kopiert Stile aus der angegebenen Vorlage in ein Dokument. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate_1)(string) | Kopiert Stile aus der angegebenen Vorlage in ein Dokument. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum)() | Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting)() | Wandelt die in Tabellenstilen angegebene Formatierung in direkte Formatierung für Tabellen im Dokument um. |
| [ExtractPages](../../aspose.words/document/extractpages)(int, int) | Gibt die zurück[`Document`](../document) Objekt, das einen bestimmten Seitenbereich darstellt. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| [GetPageInfo](../../aspose.words/document/getpageinfo)(int) | Ruft die Seitengröße, Ausrichtung und andere Informationen zu einer Seite ab, die zum Drucken oder Rendern nützlich sein könnten. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool, ImportFormatMode) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting)() | Verbindet Läufe mit derselben Formatierung in allen Absätzen des Dokuments. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes)() | Ändert Feldtypwerte[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype) von[`FieldStart`](../../aspose.words.fields/fieldstart) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator) ,[`FieldEnd`](../../aspose.words.fields/fieldend) im gesamten Dokument, damit sie den in den Feldcodes enthaltenen Feldtypen entsprechen. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Print](../../aspose.words/document/print#print)() | Druckt das gesamte Dokument auf dem Standarddrucker. |
| [Print](../../aspose.words/document/print#print_1)(PrinterSettings) | Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche). |
| [Print](../../aspose.words/document/print#print_3)(string) | Drucken Sie das gesamte Dokument auf dem angegebenen Drucker, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche). |
| [Print](../../aspose.words/document/print#print_2)(PrinterSettings, string) | Druckt das Dokument gemäß den angegebenen Druckereinstellungen, unter Verwendung des Standarddruckcontrollers (ohne Benutzeroberfläche) und eines Dokumentnamens. |
| [Protect](../../aspose.words/document/protect#protect)(ProtectionType) | Schützt das Dokument vor Änderungen ohne das bestehende Passwort zu ändern oder vergibt ein zufälliges Passwort. |
| [Protect](../../aspose.words/document/protect#protect_1)(ProtectionType, string) | Schützt das Dokument vor Änderungen und setzt optional ein Schutzkennwort. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences)() | Entfernt externe XML-Schemareferenzen aus diesem Dokument. |
| [RemoveMacros](../../aspose.words/document/removemacros)() | Entfernt alle Makros (das VBA-Projekt) sowie Symbolleisten und Befehlsanpassungen aus dem Dokument. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag) Nachkommenknoten des aktuellen Knotens. |
| [RenderToScale](../../aspose.words/document/rendertoscale)(int, Graphics, float, float, float) | Rendert eine Dokumentseite in aGraphics Objekt in einem bestimmten Maßstab. |
| [RenderToSize](../../aspose.words/document/rendertosize)(int, Graphics, float, float, float, float) | Rendert eine Dokumentseite in aGraphics Objekt auf eine bestimmte Größe. |
| [Save](../../aspose.words/document/save#save_2)(string) | Speichert das Dokument in einer Datei. Ermittelt automatisch das Speicherformat aus der Erweiterung. |
| [Save](../../aspose.words/document/save#save)(Stream, SaveFormat) | Speichert das Dokument unter Verwendung des angegebenen Formats in einem Stream. |
| [Save](../../aspose.words/document/save#save_1)(Stream, SaveOptions) | Speichert das Dokument unter Verwendung der angegebenen Speicheroptionen in einem Stream. |
| [Save](../../aspose.words/document/save#save_3)(string, SaveFormat) | Speichert das Dokument in einer Datei im angegebenen Format. |
| [Save](../../aspose.words/document/save#save_4)(string, SaveOptions) | Speichert das Dokument unter Verwendung der angegebenen Speicheroptionen in einer Datei. |
| [Save](../../aspose.words/document/save#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Sendet das Dokument an den Client-Browser. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions)(string) | Beginnt automatisch damit, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions_1)(string, DateTime) | Beginnt automatisch damit, alle weiteren Änderungen, die Sie programmgesteuert am Dokument vornehmen, als Revisionsänderungen zu markieren. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions)() | Stoppt das automatische Markieren von Dokumentänderungen als Revisionen. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |
| [UnlinkFields](../../aspose.words/document/unlinkfields)() | Hebt die Verknüpfung von Feldern im gesamten Dokument auf. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect_1)() | Entfernt den Schutz des Dokuments unabhängig vom Passwort. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect)(string) | Entfernt den Schutz des Dokuments, wenn ein korrektes Passwort angegeben wird. |
| [UpdateFields](../../aspose.words/document/updatefields)() | Aktualisiert die Werte von Feldern im gesamten Dokument. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels)() | Aktualisiert Listenbezeichnungen für alle Listenelemente im Dokument. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout)() | Baut das Seitenlayout des Dokuments neu auf. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail)() | Aktualisierungen[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) des Dokuments mit Standardoptionen. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail_1)(ThumbnailGeneratingOptions) | Aktualisierungen[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) des Dokuments gemäß den angegebenen Optionen. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount)() | Aktualisiert die Eigenschaften der Wortanzahl des Dokuments. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount_1)(bool) | Aktualisiert die Wortzähleigenschaften des Dokuments, optional aktualisiert[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines) Eigentum. |

### Bemerkungen

Das **Dokumentieren** ist ein zentrales Objekt in der Aspose.Words-Bibliothek.

Um ein vorhandenes Dokument in eines der zu laden[`LoadFormat`](../loadformat) übergeben Sie einen Dateinamen oder einen Stream an eines der Formate **Dokumentieren** Konstrukteure. Um ein leeres Dokument zu erstellen, rufen Sie den Konstruktor ohne Parameter auf.

Verwenden Sie eine der Save-Methodenüberladungen, um das Dokument in einem der [`SaveFormat`](../saveformat) Formate.

Um Dokumentseiten direkt auf eine zu zeichnen **Grafik** Objekt verwenden [`RenderToScale`](./rendertoscale) oder[`RenderToSize`](./rendertosize) Methode.

Verwenden Sie zum Drucken des Dokuments eines der[`Print`](./print)Methoden.

[`MailMerge`](./mailmerge) ist die Berichts-Engine von Aspose.Words, die es ermöglicht, Berichte, die in Microsoft Word entworfen wurden, schnell und einfach mit Daten aus verschiedenen Datenquellen zu füllen. Die Daten können aus einem DataSet, einer DataTable, einer DataView, einem IDataReader oder einem Array von Werten stammen.  **Seriendruck** wird die in der Datenquelle gefundenen Datensätze durchgehen und sie in Serienbrieffelder im Dokument einfügen, um es nach Bedarf zu vergrößern.

**Dokumentieren** speichert dokumentweite Informationen wie z[`Styles`](../documentbase/styles) , [`BuiltInDocumentProperties`](./builtindocumentproperties) ,[`CustomDocumentProperties`](./customdocumentproperties) , Listen und Makros. Auf die meisten dieser Objekte kann über die entsprechenden Eigenschaften der zugegriffen werden **Dokumentieren**.

Das **Dokumentieren**ist ein Wurzelknoten eines Baums, der alle anderen Knoten des Dokuments enthält. Der Baum ist ein zusammengesetztes Entwurfsmuster und in vielerlei Hinsicht ähnlich wie XmlDocument. Der Inhalt des Dokuments kann programmgesteuert frei manipuliert werden:

* Auf die Knoten des Dokuments kann beispielsweise über typisierte Sammlungen zugegriffen werden[`Sections`](./sections) , [`ParagraphCollection`](../paragraphcollection) usw.
* Die Knoten des Dokuments können anhand ihres Knotentyps mit ausgewählt werden.[`GetChildNodes`](../compositenode/getchildnodes) oder über eine XPath-Abfrage mit[`SelectNodes`](../compositenode/selectnodes) oder[`SelectSingleNode`](../compositenode/selectsinglenode).
* Inhaltsknoten können überall im Dokument mit hinzugefügt oder entfernt werden.[`InsertBefore`](../compositenode/insertbefore) ,[`InsertAfter`](../compositenode/insertafter) , [`RemoveChild`](../compositenode/removechild) und andere Methoden, die von der Basisklasse bereitgestellt werden[`CompositeNode`](../compositenode).
* Die Formatierungsattribute jedes Knotens können über die Eigenschaften dieses Knotens geändert werden.

Erwägen Sie die Verwendung[`DocumentBuilder`](../documentbuilder) das vereinfacht die Aufgabe, programmgesteuert zu erstellen oder den Dokumentbaum zu füllen.

Das **Dokumentieren** kann nur enthalten[`Section`](../section) Objekte.

In Microsoft Word muss ein gültiges Dokument mindestens einen Abschnitt haben.

### Beispiele

Zeigt, wie ein Seriendruck mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Im Folgenden finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Seriendruck zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um ein Ausgabe-Seriendruckdokument für jede Zeile in der Tabelle zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Seriendruckdokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Seriendruck-Quelldokument.
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

* class [DocumentBase](../documentbase)
* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
