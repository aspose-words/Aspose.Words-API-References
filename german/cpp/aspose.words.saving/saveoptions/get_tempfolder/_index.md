---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder Methode"
linktitle: "get_TempFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder Methode. Gibt den Ordner für temporäre Dateien an, die beim Speichern in eine DOC- oder DOCX-Datei verwendet werden. Standardmäßig ist diese Eigenschaft null und es werden in C++ keine temporären Dateien verwendet."
type: docs
weight: 15000
url: /de/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Gibt den Ordner für temporäre Dateien an, die beim Speichern in eine DOC‑ oder DOCX‑Datei verwendet werden. Standardmäßig ist diese Eigenschaft **null** und es werden keine temporären Dateien verwendet.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Hinweise


Wenn Aspose.Words ein Dokument speichert, muss es temporäre interne Strukturen erstellen. Standardmäßig werden diese internen Strukturen im Speicher erstellt und die Speichernutzung steigt für kurze Zeit an, während das Dokument gespeichert wird. Nach Abschluss des Speichervorgangs wird der Speicher freigegeben und vom Garbage Collector zurückgeholt.

Die Angabe eines temporären Ordners mittels [TempFolder](./) bewirkt, dass Aspose.Words die internen Strukturen in temporären Dateien anstatt im Speicher hält. Dies reduziert die Speichernutzung während des Speichervorgangs, kann jedoch die Speicherleistung verringern.

Der Ordner muss existieren und beschreibbar sein, sonst wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn das Speichern abgeschlossen ist.

## Beispiele



Zeigt, wie beim Speichern eines Dokuments die Festplatte anstelle des Speichers verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Beim Speichern eines Dokuments werden verschiedene Elemente vorübergehend im Speicher abgelegt, während der Speichervorgang stattfindet.
// Wir können diese Option verwenden, um stattdessen einen temporären Ordner im lokalen Dateisystem zu nutzen,
// was den Speicheraufwand unserer Anwendung reduziert.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Der angegebene temporäre Ordner muss im lokalen Dateisystem existieren, bevor der Speichervorgang gestartet wird.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// Der Ordner bleibt erhalten, ohne dass Restinhalte vom Ladevorgang zurückbleiben.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
