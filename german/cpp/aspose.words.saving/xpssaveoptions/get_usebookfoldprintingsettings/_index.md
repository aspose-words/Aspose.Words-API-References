---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings Methode"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings Methode. Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, wenn es über MultiplePages in C++ angegeben ist."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, wenn es über [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/) angegeben ist.

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Hinweise


Wenn diese Option angegeben ist, wird [PageSet](../../fixedpagesaveoptions/get_pageset/) beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn die Buchfalten-Druckeinstellungen im Seitenlayout nicht angegeben sind, hat diese Option keine Wirkung.

## Beispiele



Zeigt, wie man ein Dokument im XPS-Format in Form eines Buchfalz speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Setzen Sie die Eigenschaft \"UseBookFoldPrintingSettings\" auf \"true\", um den Inhalt anzuordnen
// Im ausgegebenen XPS auf eine Weise, die uns hilft, es zu einem Heft zu machen.
// Setze die "UseBookFoldPrintingSettings"-Eigenschaft auf "false", um das XPS normal zu rendern.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Wenn wir das Dokument als Heft rendern, müssen wir die \"MultiplePages\"-Eigenschaft setzen
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf \"MultiplePagesType.BookFoldPrinting\".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// Sobald wir dieses Dokument drucken, können wir es durch Stapeln der Seiten zu einem Heft machen.
// aus dem Drucker zu kommen und in der Mitte zu falten.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## Siehe auch

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
