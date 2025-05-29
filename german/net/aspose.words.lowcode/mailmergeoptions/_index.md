---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.MailMergeOptions für nahtlose Low-Code-Serienbrieflösungen. Verbessern Sie Ihre Dokumentenautomatisierung mit anpassbaren Funktionen!
type: docs
weight: 4260
url: /de/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Stellt Optionen für die Serienbrieffunktion dar.

```csharp
public class MailMergeOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Ruft eine Reihe von Flags ab oder legt diese fest, die angeben, welche Elemente während der Seriendruckfunktion entfernt werden sollen. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, ob Absätze mit Satzzeichen als leer betrachtet werden und entfernt werden sollen, wenn dieRemoveEmptyParagraphs Option angegeben ist. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob beim Ausführen eines Seriendrucks mit Regionen für die Datenquelle alle Seriendruckregionen des Dokuments mit dem Namen einer Datenquelle oder nur die erste zusammengeführt werden sollen. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Seriendrucks mit Regionen aktualisiert werden. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die nicht verwendeten „Mustache“-Tags beibehalten werden sollen. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Ruft ein Endtag für den Seriendruckbereich ab oder legt dieses fest. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Ruft ein Starttag für den Seriendruckbereich ab oder legt dieses fest. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Listen nach der Ausführung eines Seriendrucks in jedem Abschnitt neu gestartet werden. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Abschnittsanfang des ersten Dokumentabschnitts und seine Kopien für nachfolgende Datenquellenzeilen beim Seriendruck beibehalten oder entsprechend dem Verhalten von MS Word aktualisiert werden. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob nachstehende und führende Leerzeichen aus Serienbriefwerten entfernt werden. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | Wann`WAHR` , gibt an, dass Serienbriefe zusätzlich zu MERGEFIELD-Feldern auch in einigen anderen Feldtypen und auch in "{{fieldName}}"-Tags ausgeführt werden. |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Ruft einen Wert ab oder setzt ihn, der angibt, ob der ganze Absatz mit**TischStart** oder**Tabellenende** field oder bestimmter Bereich zwischen**TischStart** Und**Tabellenende** Felder sollten in den Serienbriefbereich aufgenommen werden. |

## Beispiele

Zeigt, wie Sie einen Serienbriefvorgang für einen einzelnen Datensatz durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Siehe auch

* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
