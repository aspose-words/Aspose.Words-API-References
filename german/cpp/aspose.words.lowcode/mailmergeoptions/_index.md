---
title: "Aspose::Words::LowCode::MailMergeOptions class"
linktitle: "MailMergeOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::MailMergeOptions class. Stellt Optionen für die Seriendruck‑Funktionalität in C++ dar."
type: docs
weight: 750
url: /de/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Stellt Optionen für die Seriendruck‑Funktionalität dar.

```cpp
class MailMergeOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Ruft einen Satz von Flags ab, der angibt, welche Elemente während des Seriendrucks entfernt werden sollen. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Ruft den Wert ab oder legt ihn fest, der angibt, ob Absätze mit Satzzeichen als leer betrachtet werden und entfernt werden sollen, wenn die Option [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/) angegeben ist. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Ruft einen Wert ab, der angibt, ob alle Mail‑Merge‑Regionen des Dokuments mit dem Namen einer Datenquelle beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen gegen die Datenquelle zusammengeführt werden sollen oder nur die erste. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Ruft einen Wert ab, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen aktualisiert werden. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Ruft einen Wert ab, der angibt, ob die nicht verwendeten "mustache"‑Tags erhalten bleiben sollen. |
| [get_RegionEndTag](./get_regionendtag/)() const | Ruft das End‑Tag einer Mail‑Merge‑Region ab. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Ruft das Start‑Tag einer Mail‑Merge‑Region ab. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Ruft einen Wert ab, der angibt, ob Listen nach dem Ausführen eines Mail‑Merge‑Vorgangs in jedem Abschnitt neu gestartet werden. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Ruft einen Wert ab, der angibt, ob der Abschnittsbeginn des ersten Dokumentabschnitts und dessen Kopien für nachfolgende Datenquellenzeilen während des Mail‑Merge beibehalten oder gemäß dem Verhalten von MS Word aktualisiert werden. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Ruft einen Wert ab, der angibt, ob führende und nachfolgende Leerzeichen aus Mail‑Merge‑Werten entfernt werden. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Ruft einen Wert ab, der angibt, ob Merge‑Felder und Merge‑Regionen zusammengeführt werden, unabhängig von der Bedingung des übergeordneten IF‑Feldes. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Wenn **true**, gibt an, dass neben MERGEFIELD‑Feldern der Seriendruck auch in einige andere Feldtypen und in "{{fieldName}}"‑Tags durchgeführt wird. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Ruft einen Wert ab, der angibt, ob ein ganzer Absatz mit dem **TableStart**‑ oder **TableEnd**‑Feld bzw. ein bestimmter Bereich zwischen **TableStart**‑ und **TableEnd**‑Feldern in die Mail‑Merge‑Region eingeschlossen werden soll. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Legt einen Satz von Flags fest, die angeben, welche Elemente während des Seriendrucks entfernt werden sollen. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Setter für [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Legt einen Wert fest, der angibt, ob alle Mail‑Merge‑Regionen des Dokuments mit dem Namen einer Datenquelle beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen gegen die Datenquelle zusammengeführt werden sollen oder nur die erste. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Legt einen Wert fest, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen aktualisiert werden. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Legt einen Wert fest, der angibt, ob die nicht verwendeten "mustache"‑Tags erhalten bleiben sollen. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Legt das End‑Tag einer Mail‑Merge‑Region fest. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Legt das Start‑Tag einer Mail‑Merge‑Region fest. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Legt einen Wert fest, der angibt, ob Listen nach dem Ausführen eines Mail‑Merge‑Vorgangs in jedem Abschnitt neu gestartet werden. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Legt einen Wert fest, der angibt, ob der Abschnittsbeginn des ersten Dokumentabschnitts und dessen Kopien für nachfolgende Datenquellenzeilen während des Mail‑Merge beibehalten oder gemäß dem Verhalten von MS Word aktualisiert werden. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Legt einen Wert fest, der angibt, ob führende und nachfolgende Leerzeichen aus Mail‑Merge‑Werten entfernt werden. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Legt einen Wert fest, der angibt, ob Merge‑Felder und Merge‑Regionen zusammengeführt werden, unabhängig von der Bedingung des übergeordneten IF‑Feldes. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Setter für [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Legt einen Wert fest, der angibt, ob der gesamte Absatz mit dem **TableStart**- oder **TableEnd**-Feld oder ein bestimmter Bereich zwischen den **TableStart**- und **TableEnd**-Feldern in die Seriendruckregion aufgenommen werden soll. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
