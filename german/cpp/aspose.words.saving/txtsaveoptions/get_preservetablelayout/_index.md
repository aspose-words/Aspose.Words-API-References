---
title: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout-Methode"
linktitle: "get_PreserveTableLayout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout-Methode. Gibt an, ob das Programm versuchen soll, das Layout von Tabellen beim Speichern im Nur-Text-Format beizubehalten. Der Standardwert ist false in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


Gibt an, ob das Programm beim Speichern im Klartextformat versuchen soll, das Tabellenlayout beizubehalten. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## Beispiele



Zeigt, wie das Layout von Tabellen beim Konvertieren in Nur-Text beibehalten wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument in Klartext speichern.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Setzen Sie die Eigenschaft "PreserveTableLayout" auf "true", um Leerzeichen‑Auffüllung auf den Inhalt anzuwenden
// des ausgegebenen Nur-Text-Dokuments, um das Layout der Tabelle so weit wie möglich beizubehalten.
// Setzen Sie die Eigenschaft "PreserveTableLayout" auf "false", um den Inhalt aller Tabellen zu speichern
// als zusammenhängenden Textkörper, wobei für jede Zeile nur ein Zeilenumbruch verwendet wird.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## Siehe auch

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
