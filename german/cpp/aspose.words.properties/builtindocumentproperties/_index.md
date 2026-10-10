---
title: "Aspose::Words::Properties::BuiltInDocumentProperties Klasse"
linktitle: "BuiltInDocumentProperties"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties class. Eine Sammlung von integrierten Dokumenteigenschaften. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/
---
## BuiltInDocumentProperties class


Eine Sammlung integrierter Dokumenteigenschaften. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class BuiltInDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](../documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Gibt **true** zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung existiert. |
| [get_Author](./get_author/)() | Liest oder setzt den Namen des Autors des Dokuments. |
| [get_Bytes](./get_bytes/)() | Stellt eine Schätzung der Anzahl von Bytes im Dokument dar. |
| [get_Category](./get_category/)() | Liest oder setzt die Kategorie des Dokuments. |
| [get_Characters](./get_characters/)() | Stellt eine Schätzung der Anzahl von Zeichen im Dokument dar. |
| [get_CharactersWithSpaces](./get_characterswithspaces/)() | Stellt eine Schätzung der Anzahl von Zeichen (einschließlich Leerzeichen) im Dokument dar. |
| [get_Comments](./get_comments/)() | Liest oder setzt die Dokumentkommentare. |
| [get_Company](./get_company/)() | Liest oder setzt die Firmen‑Eigenschaft. |
| [get_ContentStatus](./get_contentstatus/)() | Liest den Inhaltsstatus des Dokuments. |
| [get_ContentType](./get_contenttype/)() | Liest den Inhaltstyp des Dokuments. |
| [get_Count](../documentpropertycollection/get_count/)() | Ermittelt die Anzahl der Elemente in der Sammlung. |
| [get_CreatedTime](./get_createdtime/)() | Liest oder setzt das Erstellungsdatum des Dokuments in UTC. |
| [get_HeadingPairs](./get_headingpairs/)() | Gibt Dokumentüberschriften und deren Namen an. |
| [get_HyperlinkBase](./get_hyperlinkbase/)() | Gibt die Basiszeichenfolge an, die für die Bewertung relativer Hyperlinks in diesem Dokument verwendet wird. |
| [get_HyperlinksChanged](./get_hyperlinkschanged/)() | Gibt an, ob Hyperlinks in einem Dokument geändert wurden. |
| [get_Keywords](./get_keywords/)() | Liest oder setzt die Dokument‑Schlüsselwörter. |
| [get_LastPrinted](./get_lastprinted/)() | Liest oder setzt das Datum, an dem das Dokument zuletzt in UTC gedruckt wurde. |
| [get_LastSavedBy](./get_lastsavedby/)() | Liest oder setzt den Namen des letzten Autors. |
| [get_LastSavedTime](./get_lastsavedtime/)() | Liest oder setzt die Zeit der letzten Speicherung in UTC. |
| [get_Lines](./get_lines/)() | Stellt eine Schätzung der Zeilenanzahl im Dokument dar. |
| [get_LinksUpToDate](./get_linksuptodate/)() | Gibt an, ob Hyperlinks in einem Dokument aktuell sind. |
| [get_Manager](./get_manager/)() | Liest oder setzt die Manager‑Eigenschaft. |
| [get_NameOfApplication](./get_nameofapplication/)() | Liest oder setzt den Namen der Anwendung. |
| [get_Pages](./get_pages/)() | Stellt eine Schätzung der Seitenanzahl im Dokument dar. |
| [get_Paragraphs](./get_paragraphs/)() | Stellt eine Schätzung der Absatzanzahl im Dokument dar. |
| [get_RevisionNumber](./get_revisionnumber/)() | Liest oder setzt die Revisionsnummer des Dokuments. |
| [get_ScaleCrop](./get_scalecrop/)() | Gibt an, ob das Dokumentenvorschaubild beschnitten oder skaliert wird, um in die Anzeige zu passen. |
| [get_Security](./get_security/)() | Gibt das Sicherheitsniveau eines Dokuments als numerischen Wert an. |
| [get_SharedDocument](./get_shareddocument/)() | Gibt an, ob das Dokument ein freigegebenes Dokument ist. |
| [get_Subject](./get_subject/)() | Liest oder setzt den Betreff des Dokuments. |
| [get_Template](./get_template/)() | Liest oder setzt den informativen Namen der Dokumentvorlage. |
| [get_Thumbnail](./get_thumbnail/)() | Liest oder setzt das Vorschaubild des Dokuments. |
| [get_Title](./get_title/)() | Liest oder setzt den Titel des Dokuments. |
| [get_TitlesOfParts](./get_titlesofparts/)() | Jeder String im Array gibt den Namen eines Teils im Dokument an. |
| [get_TotalEditingTime](./get_totaleditingtime/)() | Liest oder setzt die gesamte Bearbeitungszeit in Minuten. |
| [get_Version](./get_version/)() | Stellt die Versionsnummer der Anwendung dar, die das Dokument erstellt hat. |
| [get_Words](./get_words/)() | Stellt eine Schätzung der Wortanzahl im Dokument dar. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(System::String) override | Gibt ein [DocumentProperty](../documentproperty/)-Objekt anhand des Namens der Eigenschaft zurück. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Gibt ein [DocumentProperty](../documentproperty/)-Objekt anhand des Index zurück. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Ermittelt den Index einer Eigenschaft anhand ihres Namens. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Entfernt eine Eigenschaft am angegebenen Index. |
| [set_Author](./set_author/)(const System::String\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Author](./get_author/). |
| [set_Bytes](./set_bytes/)(int32_t) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Bytes](./get_bytes/). |
| [set_Category](./set_category/)(const System::String\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Category](./get_category/). |
| [set_Characters](./set_characters/)(int32_t) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters](./get_characters/). |
| [set_CharactersWithSpaces](./set_characterswithspaces/)(int32_t) | Stellt eine Schätzung der Anzahl von Zeichen (einschließlich Leerzeichen) im Dokument dar. |
| [set_Comments](./set_comments/)(const System::String\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments](./get_comments/). |
| [set_Company](./set_company/)(const System::String\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Company](./get_company/). |
| [set_ContentStatus](./set_contentstatus/)(const System::String\&) | Setzt den Inhaltsstatus des Dokuments. |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Setzt den Inhaltstyp des Dokuments. |
| [set_CreatedTime](./set_createdtime/)(System::DateTime) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime](./get_createdtime/). |
| [set_HeadingPairs](./set_headingpairs/)(const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs](./get_headingpairs/). |
| [set_HyperlinkBase](./set_hyperlinkbase/)(const System::String\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase](./get_hyperlinkbase/). |
| [set_Keywords](./set_keywords/)(const System::String\&) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords](./get_keywords/). |
| [set_LastPrinted](./set_lastprinted/)(System::DateTime) | Setzer für [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted](./get_lastprinted/). |
| [set_LastSavedBy](./set_lastsavedby/)(const System::String\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedBy](./get_lastsavedby/). |
| [set_LastSavedTime](./set_lastsavedtime/)(System::DateTime) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime](./get_lastsavedtime/). |
| [set_Lines](./set_lines/)(int32_t) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines](./get_lines/). |
| [set_LinksUpToDate](./set_linksuptodate/)(bool) | Gibt an, ob Hyperlinks in einem Dokument aktuell sind. |
| [set_Manager](./set_manager/)(const System::String\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Manager](./get_manager/). |
| [set_NameOfApplication](./set_nameofapplication/)(const System::String\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication](./get_nameofapplication/). |
| [set_Pages](./set_pages/)(int32_t) | Stellt eine Schätzung der Seitenanzahl im Dokument dar. |
| [set_Paragraphs](./set_paragraphs/)(int32_t) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Paragraphs](./get_paragraphs/). |
| [set_RevisionNumber](./set_revisionnumber/)(int32_t) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber](./get_revisionnumber/). |
| [set_Security](./set_security/)(Aspose::Words::Properties::DocumentSecurity) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Security](./get_security/). |
| [set_Subject](./set_subject/)(const System::String\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Subject](./get_subject/). |
| [set_Template](./set_template/)(const System::String\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Template](./get_template/). |
| [set_Thumbnail](./set_thumbnail/)(const System::ArrayPtr\<uint8_t\>\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail](./get_thumbnail/). |
| [set_Title](./set_title/)(const System::String\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Title](./get_title/). |
| [set_TitlesOfParts](./set_titlesofparts/)(const System::ArrayPtr\<System::String\>\&) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts](./get_titlesofparts/). |
| [set_TotalEditingTime](./set_totaleditingtime/)(int32_t) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_TotalEditingTime](./get_totaleditingtime/). |
| [set_Version](./set_version/)(int32_t) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Version](./get_version/). |
| [set_Words](./set_words/)(int32_t) | Setter für [Aspose::Words::Properties::BuiltInDocumentProperties::get_Words](./get_words/). |
| static [Type](./type/)() |  |
## Hinweise


Stellt Zugriff auf [DocumentProperty](../documentproperty/) Objekte über ihre Namen (unter Verwendung eines Indexers) und über eine Menge typisierter Eigenschaften bereit, die Werte des entsprechenden Typs zurückgeben.

Die Namen der Eigenschaften sind nicht zwischen Groß- und Kleinschreibung unterscheidend.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.

## Beispiele



Zeigt, wie man mit integrierten Dokumenteigenschaften arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Das "Document"-Objekt enthält einige seiner Metadaten in seinen Mitgliedern.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Das Dokument speichert Metadaten auch in seinen integrierten Eigenschaften.
// Jede integrierte Eigenschaft ist ein Mitglied des "BuiltInDocumentProperties"-Objekts des Dokuments.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Einige Eigenschaften können mehrere Werte speichern.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## Siehe auch

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
