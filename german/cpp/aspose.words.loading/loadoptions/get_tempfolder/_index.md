---
title: "Aspose::Words::Loading::LoadOptions::get_TempFolder Methode"
linktitle: "get_TempFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_TempFolder Methode. Ermöglicht die Verwendung temporärer Dateien beim Lesen eines Dokuments. Standardmäßig ist diese Eigenschaft null und es werden keine temporären Dateien in C++ verwendet."
type: docs
weight: 16000
url: /de/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Ermöglicht die Verwendung temporärer Dateien beim Lesen eines Dokuments. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Hinweise


Der Ordner muss existieren und beschreibbar sein, sonst wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn das Lesen abgeschlossen ist.

## Beispiele



Zeigt, wie ein Dokument mit temporären Dateien geladen wird.
```cpp
// Beachten Sie, dass ein solcher Ansatz den Speicherverbrauch reduzieren, aber die Geschwindigkeit verringern kann
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Stellen Sie sicher, dass das Verzeichnis existiert, und laden Sie es
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Zeigt, wie beim Laden eines Dokuments die Festplatte anstelle des Speichers verwendet wird.
```cpp
// Wenn wir ein Dokument laden, werden verschiedene Elemente vorübergehend im Speicher abgelegt, während der Speichervorgang ausgeführt wird.
// Wir können diese Option verwenden, um stattdessen einen temporären Ordner im lokalen Dateisystem zu nutzen,
// was den Speicheraufwand unserer Anwendung reduziert.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Der angegebene temporäre Ordner muss im lokalen Dateisystem vorhanden sein, bevor der Ladevorgang gestartet wird.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// Der Ordner bleibt erhalten, ohne dass Restinhalte vom Ladevorgang zurückbleiben.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Siehe auch

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
