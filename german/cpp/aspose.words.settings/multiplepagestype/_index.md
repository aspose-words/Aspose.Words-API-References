---
title: "Aspose::Words::Settings::MultiplePagesType Enum"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::MultiplePagesType Enum. Gibt an, wie das Dokument in C++ gedruckt wird."
type: docs
weight: 18000
url: /de/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Gibt an, wie das Dokument gedruckt wird.

```cpp
enum class MultiplePagesType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | 0 | Normaler Druck, keine Mehrseitendrucke angegeben. |
| MirrorMargins | 1 | Vertauscht linke und rechte Ränder auf gegenüberliegenden Seiten. |
| TwoPagesPerSheet | 2 | Druckt zwei Seiten pro Blatt. |
| BookFoldPrinting | 3 | Gibt an, ob das Dokument als Buchfalz gedruckt werden soll. |
| BookFoldPrintingReverse | 4 | Gibt an, ob das Dokument als umgekehrter Buchfalz gedruckt werden soll. |
| Default | n/a | Standardwert ist [Normal](./) |


## Beispiele



Zeigt, wie ein Dokument konfiguriert wird, das als Buchfalz gedruckt werden kann.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügt Text ein, der sich über 16 Seiten erstreckt.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Konfigurieren Sie die "PageSetup"-Eigenschaft des ersten Abschnitts, um das Dokument in Form eines Buchfalz zu drucken.
// Wenn wir dieses Dokument beidseitig drucken, können wir die Seiten nehmen, um sie zu stapeln
// und sie alle gleichzeitig in der Mitte falten. Der Inhalt des Dokuments wird zu einem Buchfalz ausgerichtet.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Wir können die Anzahl der Blätter nur in Vielfachen von 4 angeben.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
