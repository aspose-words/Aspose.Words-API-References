---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat Methode"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat Methode. Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses SaveOptions-Objekt verwendet wird. Kann nur Ps in C++ sein."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionen-Objekt verwendet wird. Kann nur [Ps](../../../aspose.words/saveformat/) sein.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


## Beispiele



Zeigt, wie man ein Dokument im Postscript-Format in Form eines Buchfalz speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Erstellen Sie ein \"PsSaveOptions\"-Objekt, das wir an die \"Save\"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in PostScript konvertiert.
// Setzen Sie die Eigenschaft \"UseBookFoldPrintingSettings\" auf \"true\", um den Inhalt anzuordnen
// im ausgegebenen Postscript-Dokument auf eine Weise, die es uns ermöglicht, daraus ein Heft zu erstellen.
// Setzen Sie die Eigenschaft \"UseBookFoldPrintingSettings\" auf \"false\", um das Dokument normal zu speichern.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Wenn wir das Dokument als Heft rendern, müssen wir die \"MultiplePages\"-Eigenschaft setzen
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf \"MultiplePagesType.BookFoldPrinting\".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Sobald wir dieses Dokument beidseitig drucken, können wir alle Seiten gleichzeitig in der Mitte falten,
// und der Inhalt wird sich so ausrichten, dass ein Heft entsteht.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
