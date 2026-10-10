---
title: "Aspose::Words::Settings::MailMergeSettings class"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::MailMergeSettings class. Gibt alle Seriendruckinformationen für ein Dokument an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Gibt alle Seriendruckinformationen für ein Dokument an. Weitere Informationen finden Sie im Dokumentationsartikel [Seriendruck und Berichterstellung](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Löscht die Seriendruckeinstellungen so, dass beim Speichern des Dokuments keine Seriendruckeinstellungen gespeichert werden und es zu einem normalen Dokument wird. |
| [Clone](./clone/)() | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [get_ActiveRecord](./get_activerecord/)() const | Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. Der Standardwert ist 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Gibt die Spalte in der Datenquelle an, die E-Mail-Adressen enthält. Der Standardwert ist eine leere Zeichenfolge. |
| [get_CheckErrors](./get_checkerrors/)() const | Gibt den Typ der Fehlermeldung an, die von Microsoft Word beim Ausführen eines Seriendrucks durchgeführt wird. Der Standardwert ist [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Gibt die Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |
| [get_DataSource](./get_datasource/)() const | Gibt den Pfad zur Seriendruck-Datenquelle an. Der Standardwert ist eine leere Zeichenfolge. |
| [get_DataType](./get_datatype/)() const | Gibt den Typ der Seriendruck-Datenquelle und die Zugriffsart an. Der Standardwert ist [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Gibt an, wie Microsoft Word die Ergebnisse eines Seriendrucks ausgibt. Der Standardwert ist [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Gibt an, wie eine Anwendung, die den Seriendruck ausführt, mit Leerzeilen in den aus dem Seriendruck resultierenden zusammengeführten Dokumenten umgehen soll. Der Standardwert ist **false**. |
| [get_HeaderSource](./get_headersource/)() const | Gibt den Pfad zur Seriendruck-Header-Quelle an. Der Standardwert ist eine leere Zeichenfolge. |
| [get_LinkToQuery](./get_linktoquery/)() const | Nicht sicher bei diesem. Die Microsoft Word Automation Reference legt nahe, dass dies angibt, dass die Abfrage jedes Mal ausgeführt wird, wenn das Dokument in Microsoft Word geöffnet wird. Aber die OOXML-Spezifikation legt nahe, dass dies angibt, dass die Abfrage einen Verweis auf eine externe Abfragedatei enthält, die die eigentliche Abfrage enthält. Der Standardwert ist **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Gibt an, dass die während eines Seriendruckvorgangs erzeugten Dokumente per E‑Mail als Anhang und nicht im Textkörper der eigentlichen E‑Mail gesendet werden sollen. Der Standardwert ist **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Gibt den Text an, der in der Betreffzeile der während des Seriendrucks erzeugten E‑Mails oder Faxe erscheinen soll. Der Standardwert ist eine leere Zeichenfolge. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Gibt den Hauptdokumenttyp für den Seriendruck an. Der Standardwert ist [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Ruft das Objekt ab, das die Einstellungen des Office Data Source Object (ODSO) spezifiziert. |
| [get_Query](./get_query/)() const | Enthält die Structured Query Language‑Zeichenfolge, die gegen die angegebene externe Datenquelle ausgeführt werden soll, um den Datensatz zurückzugeben, der beim Seriendruckvorgang in das Dokument importiert wird. Der Standardwert ist eine leere Zeichenfolge. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle dort anzeigen soll, wo Seriendruckfelder eingefügt wurden (z. B. Vorschau zusammengeführter Daten). Der Standardwert ist **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Gibt den einsbasierten Index des Datensatzes aus der Datenquelle an, der in Microsoft Word angezeigt werden soll. Der Standardwert ist 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Gibt die Spalte in der Datenquelle an, die E-Mail-Adressen enthält. Der Standardwert ist eine leere Zeichenfolge. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Gibt den Typ der Fehlermeldung an, die von Microsoft Word beim Ausführen eines Seriendrucks durchgeführt wird. Der Standardwert ist [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Gibt die Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Gibt den Pfad zur Seriendruck-Datenquelle an. Der Standardwert ist eine leere Zeichenfolge. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Gibt den Typ der Seriendruck-Datenquelle und die Zugriffsart an. Der Standardwert ist [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Gibt an, wie Microsoft Word die Ergebnisse eines Seriendrucks ausgibt. Der Standardwert ist [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Gibt an, wie eine Anwendung, die den Seriendruck ausführt, mit Leerzeilen in den aus dem Seriendruck resultierenden zusammengeführten Dokumenten umgehen soll. Der Standardwert ist **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Gibt den Pfad zur Seriendruck-Header-Quelle an. Der Standardwert ist eine leere Zeichenfolge. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | Setter für [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Gibt an, dass die während eines Seriendruckvorgangs erzeugten Dokumente per E‑Mail als Anhang und nicht im Textkörper der eigentlichen E‑Mail gesendet werden sollen. Der Standardwert ist **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Gibt den Text an, der in der Betreffzeile der während des Seriendrucks erzeugten E‑Mails oder Faxe erscheinen soll. Der Standardwert ist eine leere Zeichenfolge. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | Setter für [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Setzt das Objekt, das die Einstellungen des Office Data Source Object (ODSO) spezifiziert. |
| [set_Query](./set_query/)(const System::String\&) | Enthält die Structured Query Language‑Zeichenfolge, die gegen die angegebene externe Datenquelle ausgeführt werden soll, um den Datensatz zurückzugeben, der beim Seriendruckvorgang in das Dokument importiert wird. Der Standardwert ist eine leere Zeichenfolge. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Gibt an, dass Microsoft Word die Daten aus der angegebenen externen Datenquelle dort anzeigen soll, wo Seriendruckfelder eingefügt wurden (z. B. Vorschau zusammengeführter Daten). Der Standardwert ist **false**. |
| static [Type](./type/)() |  |
## Hinweise


Sie können dieses Objekt verwenden, um eine Seriendruck-Datenquelle für ein Dokument anzugeben, und diese Informationen (zusammen mit den verfügbaren Datenfeldern) werden in Microsoft Word angezeigt, wenn der Benutzer dieses Dokument öffnet. Oder Sie können dieses Objekt verwenden, um die Seriendruckeinstellungen abzufragen, die der Benutzer in Microsoft Word für dieses Dokument festgelegt hat.

Sie müssen normalerweise keine Objekte dieser Klasse direkt erstellen, da die Seriendruckeinstellungen eines Dokuments stets über die Eigenschaft [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) verfügbar sind.

Um festzustellen, ob dieses Dokument ein Hauptdokument für den Seriendruck ist, prüfen Sie den Wert der Eigenschaft [MainDocumentType](./get_maindocumenttype/).

Um Seriendruckeinstellungen und Datenquelleninformationen aus einem Dokument zu entfernen, können Sie die Methode [Clear](./clear/) verwenden. Aspose.Words schreibt keine Seriendruckeinstellungen in ein Dokument, wenn die Eigenschaft [MainDocumentType](./get_maindocumenttype/) auf [NotAMergeDocument](../mailmergemaindocumenttype/) gesetzt ist oder die Eigenschaft [DataType](./get_datatype/) auf [None](../mailmergedatatype/) gesetzt ist.

Der beste Weg, um zu lernen, wie man die Eigenschaften dieses Objekts verwendet, besteht darin, ein Dokument mit einer gewünschten Datenquelle manuell in Microsoft Word zu erstellen und dann dieses Dokument mit Aspose.Words zu öffnen und die Eigenschaften der [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) und [Odso](./get_odso/) Objekte zu untersuchen. Dies ist ein guter Ansatz, wenn Sie beispielsweise lernen möchten, wie man eine Datenquelle programmgesteuert konfiguriert.

Aspose.Words bewahrt Mail-Merge-Informationen beim Laden, Speichern und Konvertieren von Dokumenten zwischen verschiedenen Formaten, verwendet diese Informationen jedoch nicht, wenn es sein eigenes Mail-Merge mit dem [MailMerge](../../aspose.words.mailmerging/mailmerge/) Objekt durchführt.

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
