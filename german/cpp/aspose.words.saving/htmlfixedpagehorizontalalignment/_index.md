---
title: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment enum. Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTML-Dokument in C++ an."
type: docs
weight: 59000
url: /de/cpp/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enum


Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTML-Dokument an.

```cpp
enum class HtmlFixedPageHorizontalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Links | 0 | Seiten nach links ausrichten. |
| Mitte | 1 | Seiten zentrieren. Dies ist der Standardwert. |
| Rechts | 2 | Seiten nach rechts ausrichten. |


## Beispiele



Zeigt, wie man die horizontale Ausrichtung von Seiten beim Speichern eines Dokuments als HTML festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_PageHorizontalAlignment(pageHorizontalAlignment);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Center:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Left:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment::Right:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }")->get_Success());
        break;

}
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
