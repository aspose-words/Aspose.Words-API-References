---
title: "Methode Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks"
linktitle: "get_ForcePageBreaks"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks. Ermöglicht die Angabe, ob Seitenumbrüche beim Export beibehalten werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Ermöglicht die Angabe, ob Seitenumbrüche beim Export beibehalten werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Beispiele



Zeigt, wie man angibt, ob Seitenumbrüche beim Export eines Dokuments in Klartext beibehalten werden sollen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an das "Save" des Dokuments übergeben können.
// Methode, um zu ändern, wie wir das Dokument in Klartext speichern.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Die Aspose.Words "Document"-Objekte haben Seitenumbrüche, genau wie Microsoft‑Word‑Dokumente.
// Speicherformate wie ".txt" sind ein zusammenhängender Textkörper ohne Seitenumbrüche.
// Setzen Sie die "ForcePageBreaks"-Eigenschaft auf "true", um alle Seitenumbrüche in Form von '\\f'-Zeichen zu erhalten.
// Setzen Sie die "ForcePageBreaks"-Eigenschaft auf "false", um alle Seitenumbrüche zu verwerfen.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Wenn wir ein Klartextdokument mit Seitenumbrüchen laden,
// wird das "Document"-Objekt sie verwenden, um den Inhalt in Seiten zu unterteilen.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## Siehe auch

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
