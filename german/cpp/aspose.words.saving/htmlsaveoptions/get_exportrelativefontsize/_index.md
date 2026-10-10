---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize Methode"
linktitle: "get_ExportRelativeFontSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize Methode. Gibt an, ob Schriftgrößen beim Speichern in HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standardwert ist false in C++."
type: docs
weight: 25000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


Gibt an, ob Schriftgrößen beim Speichern nach HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Hinweise


In vielen bestehenden Dokumenten (HTML, IDPF EPUB) werden Schriftgrößen in relativen Einheiten angegeben. Dies ermöglicht Anwendungen, die Textgröße beim Anzeigen/Verarbeiten von Dokumenten anzupassen. Zum Beispiel hat Microsoft Internet Explorer das Untermenü "View->Text Size", Adobe Digital Editions hat zwei Schaltflächen: Increase/Decrease Text Size. Wenn Sie erwarten, dass diese Funktionalität funktioniert, setzen Sie die Eigenschaft [ExportRelativeFontSize](./) auf **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

Wenn diese Option aktiviert ist, behalten Dokumentelemente außer Text absolute Größen bei. Auch einige textbezogene Attribute können absolut ausgedrückt werden. Insbesondere kann der mit der Regel "exactly" angegebene Zeilenabstand unerwünschte Ergebnisse beim Skalieren von Text erzeugen. Daher sollten die Quelldokumente beim Export mit [ExportRelativeFontSize](./) auf **true** korrekt gestaltet und getestet werden.

## Beispiele



Zeigt, wie relative Schriftgrößen beim Speichern nach .html verwendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions‑Objekt übergeben
// um zu bestimmen, ob relative oder absolute Schriftgrößen verwendet werden sollen.
// Setzen Sie das Flag "ExportRelativeFontSize" auf "true", um Schriftgrößen zu deklarieren
// unter Verwendung der Messgröße "em", die ein Faktor ist, der die aktuelle Schriftgröße multipliziert.
// Setzen Sie das Flag "ExportRelativeFontSize" auf "false", um Schriftgrößen zu deklarieren
// unter Verwendung der Messgröße "pt", die die absolute Größe der Schrift in Punkten darstellt.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
