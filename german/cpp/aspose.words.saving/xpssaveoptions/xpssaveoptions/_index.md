---
title: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions Konstruktor"
linktitle: "XpsSaveOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions Konstruktor. Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im Xps-Format in C++ zu speichern."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Xps](../../../aspose.words/saveformat/) Format zu speichern.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Beispiele



Zeigt, wie man die Ebene der Überschriften begrenzt, die im Inhaltsverzeichnis eines gespeicherten XPS‑Dokuments erscheinen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie Überschriften ein, die als TOC‑Einträge der Ebenen 1, 2 und anschließend 3 dienen können.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Das ausgegebene XPS‑Dokument enthält ein Inhaltsverzeichnis, das die Überschriften im Dokumentkörper auflistet.
// Ein Klick auf einen Eintrag in diesem Inhaltsverzeichnis führt uns zur Position der jeweiligen Überschrift.
// Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "2", um alle Überschriften mit einer Ebene über 2 vom Inhaltsverzeichnis auszuschließen.
// Die letzten beiden oben eingefügten Überschriften werden nicht angezeigt.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Siehe auch

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument im [Xps](../../../aspose.words/saveformat/) oder [OpenXps](../../../aspose.words/saveformat/) Format zu speichern.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
