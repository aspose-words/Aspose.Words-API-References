---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix-Methode"
linktitle: "get_CssClassNamePrefix"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix-Methode. Gibt ein Präfix an, das zu allen CSS‑Klassennamen hinzugefügt wird. Der Standardwert ist ein leerer String und generierte CSS‑Klassennamen haben in C++ kein gemeinsames Präfix."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Gibt ein Präfix an, das allen CSS-Klassennamen hinzugefügt wird. Der Standardwert ist eine leere Zeichenkette und generierte CSS-Klassennamen haben kein gemeinsames Präfix.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Hinweise


Wenn dieser Wert nicht leer ist, beginnen alle von Aspose.Words erzeugten CSS‑Klassen mit dem angegebenen Präfix. Dies kann nützlich sein, zum Beispiel wenn Sie benutzerdefiniertes CSS zu erzeugten Dokumenten hinzufügen und Namenskonflikte bei Klassen verhindern möchten.

Wenn der Wert nicht **null** oder leer ist, muss er ein gültiger CSS‑Bezeichner sein.

## Beispiele



Zeigt, wie ein Dokument nach HTML gespeichert und allen CSS‑Klassennamen ein Präfix hinzugefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
