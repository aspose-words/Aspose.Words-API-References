---
title: "Aspose::Words::MailMerging::MailMerge Klasse"
linktitle: "MailMerge"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MailMerge Klasse. Stellt die Mail-Merge-Funktionalität bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Stellt die Seriendruck-Funktionalität dar. Weitere Informationen finden Sie im Dokumentationsartikel [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [DeleteFields](./deletefields/)() | Entfernt mail‑merge‑bezogene Felder aus dem Dokument. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Führt ein Mail-Merge aus einer benutzerdefinierten Datenquelle durch. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Führt einen Mail-Merge-Vorgang für einen einzelnen Datensatz durch. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Führt ein Mail-Merge aus einer benutzerdefinierten Datenquelle mit Mail-Merge-Regionen durch. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Führt ein Mail-Merge aus einer benutzerdefinierten Datenquelle mit Mail-Merge-Regionen durch. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Ruft einen Satz von Flags ab, der angibt, welche Elemente während des Seriendrucks entfernt werden sollen. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Liest oder setzt einen Wert, der angibt, ob Absätze mit Satzzeichen als leer betrachtet werden und entfernt werden sollen, wenn die Option [RemoveEmptyParagraphs](../mailmergecleanupoptions/) angegeben ist. |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Tritt beim Seriendruck auf, wenn ein Seriendruckfeld im Dokument gefunden wird. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Ermöglicht das Behandeln bestimmter Ereignisse während des Seriendrucks. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Gibt eine Sammlung zurück, die die zugeordneten Datenfelder für den Seriendruckvorgang darstellt. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Ruft einen Wert ab, der angibt, ob alle Mail‑Merge‑Regionen des Dokuments mit dem Namen einer Datenquelle beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen gegen die Datenquelle zusammengeführt werden sollen oder nur die erste. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Ruft einen Wert ab, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen aktualisiert werden. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Ruft einen Wert ab, der angibt, ob die nicht verwendeten "mustache"‑Tags erhalten bleiben sollen. |
| [get_RegionEndTag](./get_regionendtag/)() const | Ruft das End‑Tag einer Mail‑Merge‑Region ab. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Ruft das Start‑Tag einer Mail‑Merge‑Region ab. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Ruft einen Wert ab, der angibt, ob Listen nach dem Ausführen eines Mail‑Merge‑Vorgangs in jedem Abschnitt neu gestartet werden. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Ermittelt einen Wert, der angibt, ob der [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) des ersten Dokumentabschnitts und seiner Kopien für nachfolgende Datenquellenzeilen während des Seriendrucks beibehalten oder gemäß dem Verhalten von MS Word aktualisiert wird. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Ruft einen Wert ab, der angibt, ob führende und nachfolgende Leerzeichen aus Mail‑Merge‑Werten entfernt werden. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Ruft einen Wert ab, der angibt, ob Merge‑Felder und Merge‑Regionen zusammengeführt werden, unabhängig von der Bedingung des übergeordneten IF‑Feldes. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Wenn **true**, gibt an, dass neben MERGEFIELD‑Feldern der Seriendruck auch in einige andere Feldtypen und in "{{fieldName}}"‑Tags durchgeführt wird. |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Ruft einen Wert ab, der angibt, ob ein ganzer Absatz mit dem **TableStart**‑ oder **TableEnd**‑Feld bzw. ein bestimmter Bereich zwischen **TableStart**‑ und **TableEnd**‑Feldern in die Mail‑Merge‑Region eingeschlossen werden soll. |
| [GetFieldNames](./getfieldnames/)() | Gibt eine Sammlung von Seriendruckfeldnamen zurück, die im Dokument verfügbar sind. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Gibt eine Sammlung von Seriendruckfeldnamen zurück, die in der Region verfügbar sind. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Gibt eine Sammlung von Seriendruckfeldnamen zurück, die in der Region verfügbar sind. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Gibt eine Sammlung von Seriendruckregionen mit dem angegebenen Namen zurück. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Gibt die vollständige Hierarchie von Regionen (mit Feldern) zurück, die im Dokument verfügbar sind. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Legt einen Satz von Flags fest, die angeben, welche Elemente während des Seriendrucks entfernt werden sollen. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Setter für [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Tritt beim Seriendruck auf, wenn ein Seriendruckfeld im Dokument gefunden wird. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Ermöglicht das Behandeln bestimmter Ereignisse während des Seriendrucks. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Legt einen Wert fest, der angibt, ob alle Mail‑Merge‑Regionen des Dokuments mit dem Namen einer Datenquelle beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen gegen die Datenquelle zusammengeführt werden sollen oder nur die erste. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Legt einen Wert fest, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Mail‑Merge‑Vorgangs mit Regionen aktualisiert werden. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Legt einen Wert fest, der angibt, ob die nicht verwendeten "mustache"‑Tags erhalten bleiben sollen. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Legt das End‑Tag einer Mail‑Merge‑Region fest. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Legt das Start‑Tag einer Mail‑Merge‑Region fest. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Legt einen Wert fest, der angibt, ob Listen nach dem Ausführen eines Mail‑Merge‑Vorgangs in jedem Abschnitt neu gestartet werden. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Setzt einen Wert, der angibt, ob der [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) des ersten Dokumentabschnitts und seiner Kopien für nachfolgende Datenquellenzeilen während des Seriendrucks beibehalten oder gemäß dem Verhalten von MS Word aktualisiert wird. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Legt einen Wert fest, der angibt, ob führende und nachfolgende Leerzeichen aus Mail‑Merge‑Werten entfernt werden. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Legt einen Wert fest, der angibt, ob Merge‑Felder und Merge‑Regionen zusammengeführt werden, unabhängig von der Bedingung des übergeordneten IF‑Feldes. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Setter für [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Legt einen Wert fest, der angibt, ob der gesamte Absatz mit dem **TableStart**- oder **TableEnd**-Feld oder ein bestimmter Bereich zwischen den **TableStart**- und **TableEnd**-Feldern in die Seriendruckregion aufgenommen werden soll. |
| static [Type](./type/)() |  |
## Hinweise


Damit der Seriendruckvorgang funktioniert, muss das Dokument Word‑MERGEFIELD‑ und optional NEXT‑Felder enthalten. Während des Seriendrucks werden die Seriendruckfelder im Dokument durch Werte aus Ihrer Datenquelle ersetzt.

Es gibt zwei unterschiedliche Möglichkeiten, den Seriendruck zu verwenden: mit Seriendruckregionen und ohne.

Der einfachste Seriendruck erfolgt ohne Regionen und ist dem Vorgehen in Word sehr ähnlich. Verwenden Sie **Execute**‑Methoden, um Informationen aus einer Datenquelle wie **DataTable**, **DataSet** oder einem Array von Objekten in Ihr Dokument zu übernehmen. Das [MailMerge](./)‑Objekt verarbeitet alle Datensätze der Datenquelle und kopiert sowie fügt den Inhalt des gesamten Dokuments für jeden Datensatz ein.

Beachten Sie, dass das [MailMerge](./)‑Objekt bei einem NEXT‑Feld den nächsten Datensatz in der Datenquelle auswählt und das Zusammenführen fortsetzt, ohne Inhalt zu kopieren.

Verwenden Sie [ExecuteWithRegions()](../) und weitere Überladungen, um Informationen in ein Dokument mit definierten Seriendruckregionen zu übernehmen. Sie können dafür Datenquellen verwenden.

Sie müssen Seriendruckregionen verwenden, wenn Sie Teile im Dokument dynamisch erweitern möchten. Ohne Seriendruckregionen wird das gesamte Dokument für jeden Datensatz der Datenquelle wiederholt.

## Siehe auch

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
