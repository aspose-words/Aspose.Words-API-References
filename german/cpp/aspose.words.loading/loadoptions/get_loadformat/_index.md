---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat Methode"
linktitle: "get_LoadFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat Methode. Gibt das Format des zu ladenden Dokuments an. Standard ist Auto in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Gibt das Format des zu ladenden Dokuments an. Standard ist [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Hinweise


Es wird empfohlen, den Wert [Auto](../../../aspose.words/loadformat/) anzugeben und Aspose.Words das Dateiformat automatisch erkennen zu lassen. Wenn Sie das Format des Dokuments, das Sie laden möchten, kennen, können Sie das Format explizit angeben, wodurch die Ladezeit leicht reduziert wird, da der Aufwand für die automatische Format-Erkennung entfällt. Geben Sie ein explizites Ladeformat an und stellt sich heraus, dass es falsch ist, wird die automatische Erkennung aufgerufen und ein zweiter Versuch, die Datei zu laden, unternommen.

## Beispiele



Zeigt, wie man beim Öffnen eines HTML-Dokuments eine Basis-URI angibt.
```cpp
// Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das über eine relative URI verlinkt ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir die relative URI in eine absolute URI auflösen.
// Wir können eine Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Obwohl das Bild im Eingabe-.html beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Siehe auch

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
