---
title: "Aspose::Words::Font::get_StyleName metod"
linktitle: "get_StyleName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_StyleName metod. Hämtar eller anger namnet på teckenstilen som tillämpas på denna formatering i C++."
type: docs
weight: 44000
url: /sv/cpp/aspose.words/font/get_stylename/
---
## Font::get_StyleName method


Hämtar eller anger namnet på teckenstilen som tillämpas på denna formatering.

```cpp
System::String Aspose::Words::Font::get_StyleName()
```


## Exempel



Visar hur man ändrar stilen på befintlig text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan finns två sätt att referera till stilar.
// 1 -  Använd stilnamnet:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Använd en inbyggd stilidentifierare:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Konvertera alla användningar av en stil till en annan,
// använd de ovanstående metoderna för att referera till gamla och nya stilar.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
