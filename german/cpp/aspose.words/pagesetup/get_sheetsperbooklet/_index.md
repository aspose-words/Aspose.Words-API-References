---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet-Methode"
linktitle: "get_SheetsPerBooklet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet Methode. Gibt die Anzahl der Seiten zurück oder legt sie fest, die in jedem Heft enthalten sein sollen, in C++."
type: docs
weight: 42000
url: /de/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Gibt die Anzahl der Seiten zurück, die in jedem Heft enthalten sein sollen, oder legt sie fest.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
