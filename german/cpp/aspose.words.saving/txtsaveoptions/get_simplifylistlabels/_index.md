---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels-Methode"
linktitle: "get_SimplifyListLabels"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels-Methode. Gibt an, ob das Programm Listeneinträge vereinfachen soll, wenn komplexe Formatierungen nicht angemessen im Klartext dargestellt werden können. Ist der Wert true, werden nummerierte Listeneinträge im einfachen numerischen Format und Aufzählungslisten als einfache ASCII‑Zeichen geschrieben. Der Standardwert ist false in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Gibt an, ob das Programm Listeneinträge vereinfachen soll, wenn komplexe Formatierungen in Klartext nicht angemessen dargestellt werden können. Wenn **true** gesetzt ist, werden nummerierte Listeneinträge in einfachem Zahlenformat und Aufzählungspunkte als einfache ASCII‑Zeichen geschrieben. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Beispiele



Zeigt, wie das Aussehen von Listen beim Speichern eines Dokuments als Klartext geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie eine Aufzählungsliste mit fünf Einrückungsebenen.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument in Klartext speichern.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Setzen Sie die Eigenschaft "SimplifyListLabels" auf "true", um einige List
// Symbole in einfachere ASCII‑Zeichen zu konvertieren, wie '*', 'o', '+', '>', usw.
// Setzen Sie die Eigenschaft "SimplifyListLabels" auf "false", um möglichst viele ursprüngliche Listensymbole beizubehalten.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## Siehe auch

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
