---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings Methode"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob das Dokument mit einem Booklet-Drucklayout gespeichert werden soll, falls es über MultiplePages in C++ angegeben ist."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, wenn es über [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/) angegeben ist.

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Hinweise


Wenn diese Option angegeben ist, wird [PageSet](../../fixedpagesaveoptions/get_pageset/) beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn die Buchfalten-Druckeinstellungen im Seitenlayout nicht angegeben sind, hat diese Option keine Wirkung.

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

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
