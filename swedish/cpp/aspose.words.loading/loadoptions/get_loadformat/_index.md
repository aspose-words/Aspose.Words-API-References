---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat metod"
linktitle: "get_LoadFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat metod. Anger formatet för dokumentet som ska laddas. Standard är Auto i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Anger formatet för dokumentet som ska laddas. Standard är [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Anmärkningar


Det rekommenderas att du anger värdet [Auto](../../../aspose.words/loadformat/) och låter Aspose.Words upptäcka filformatet automatiskt. Om du känner till formatet på dokumentet du ska ladda, kan du ange formatet explicit och detta kommer att något minska laddningstiden genom den overhead som är förknippad med automatisk formatdetektering. Om du anger ett explicit laddningsformat och det visar sig vara felaktigt, kommer den automatiska detektionen att aktiveras och ett andra försök att ladda filen kommer att göras.

## Exempel



Visar hur man anger en bas‑URI när man öppnar ett html‑dokument.
```cpp
// Anta att vi vill läsa in ett .html‑dokument som innehåller en bild länkad med en relativ URI
// medan bilden finns på en annan plats. I så fall måste vi omvandla den relativa URI:n till en absolut.
// Vi kan ange en bas‑URI med ett HtmlLoadOptions‑objekt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Även om bilden var trasig i den inmatade .html‑filen, hjälpte vår anpassade bas‑URI oss att reparera länken.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Detta utdata‑dokument kommer att visa bilden som saknades.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Se även

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
