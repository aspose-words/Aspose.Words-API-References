---
title: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions Methode"
linktitle: "get_OutlineOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions-Methode. Ermöglicht das Festlegen von Gliederungsoptionen in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


Ermöglicht die Angabe von Umrissoptionen.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## Hinweise


Beachten Sie, dass die Option [ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) beim Speichern nach XPS nicht funktioniert.

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

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
