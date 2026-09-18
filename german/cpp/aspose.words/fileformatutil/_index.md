---
title: "Aspose::Words::FileFormatUtil Klasse"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::FileFormatUtil Klasse. Stellt Dienstprogrammmethoden für die Arbeit mit Dateiformaten bereit, z. B. zum Erkennen von Dateiformaten oder zum Konvertieren von Dateierweiterungen zu/von Dateiformat-Enums. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 28000
url: /de/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Stellt Hilfsmethoden für die Arbeit mit Dateiformaten bereit, z. B. zum Erkennen von Dateiformaten oder zum Konvertieren von Dateierweiterungen in/von Dateiformat‑Enums. Weitere Informationen finden Sie im Dokumentationsartikel [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatUtil
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Konvertiert den IANA‑Inhaltstyp in einen Aufladeformat‑Aufzählungswert. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Konvertiert den IANA‑Inhaltstyp in einen Speicherformat‑Aufzählungswert. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Erkennt und gibt die Informationen über das Format eines in einer Festplattendatei gespeicherten Dokuments zurück. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Erkennt und gibt die Informationen über das Format eines in einem Stream gespeicherten Dokuments zurück. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Konvertiert eine Dateinamenerweiterung in einen [SaveFormat](../saveformat/) Wert. |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Konvertiert einen Aspose.Words‑Bildtyp‑Aufzählungswert in eine Dateierweiterung. Die zurückgegebene Erweiterung ist ein kleingeschriebener String mit einem führenden Punkt. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Konvertiert einen Aufladeformat‑Aufzählungswert in eine Dateierweiterung. Die zurückgegebene Erweiterung ist ein kleingeschriebener String mit einem führenden Punkt. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Konvertiert einen [LoadFormat](../loadformat/) Wert in einen [SaveFormat](../saveformat/) Wert, falls möglich. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Konvertiert einen Aufzählungswert des Speicherformats in eine Dateierweiterung. Die zurückgegebene Erweiterung ist ein kleingeschriebener String mit einem führenden Punkt. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Konvertiert einen [SaveFormat](../saveformat/) Wert in einen [LoadFormat](../loadformat/) Wert, falls möglich. |

## Beispiele



Zeigt, wie die Kodierung in einer HTML-Datei erkannt wird.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Die Eigenschaft Encoding wird nur verwendet, wenn wir ein FileFormatInfo‑Objekt für ein HTML‑Dokument erstellen.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
