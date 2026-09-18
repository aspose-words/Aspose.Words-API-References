---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins Methode"
linktitle: "get_ExportPageMargins"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins Methode. Gibt an, ob Seitenränder nach HTML, MHTML oder EPUB exportiert werden. Standard ist false in C++."
type: docs
weight: 23000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Gibt an, ob Seitenränder nach HTML, MHTML oder EPUB exportiert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Beispiele



Zeigt, wie Objekte außerhalb der Grenzen in ausgegebenen HTML-Dokumenten angezeigt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie einen Builder, um eine Form ohne Textumbruch einzufügen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Negative Positionswerte der Form können die Form außerhalb der Seitenränder platzieren.
// Wenn wir dies nach HTML exportieren, wird die Form abgeschnitten dargestellt.
shape->set_Left(-150);

// Beim Speichern des Dokuments als HTML können wir ein SaveOptions‑Objekt übergeben
// um zu entscheiden, ob die Seite angepasst werden soll, um Objekte außerhalb der Grenzen vollständig anzuzeigen.
// Wenn wir das Flag "ExportPageMargins" auf "true" setzen, wird die Form im ausgegebenen HTML vollständig sichtbar sein.
// Wenn wir das Flag "ExportPageMargins" auf "false" setzen,
// wird unser Dokument die Form abgeschnitten anzeigen, wie wir sie in Microsoft Word sehen würden.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
