---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NumSpacing enum. Anger möjliga värden för hur siffrors avstånd kan visas i C++."
type: docs
weight: 103500
url: /sv/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Anger möjliga värden för hur siffraavstånd kan visas.

```cpp
enum class NumSpacing
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Standard | 0 | Anger att siffror visas i typsnittets standardform. |
| Proportionell | 1 | Anger att formerna av siffrorna som är utformade som proportionellt avstånd visas om teckensnittet stöder det. |
| Tabulär | 2 | Anger att formerna av siffrorna som är utformade som tabulära visas om teckensnittet stöder det. |


## Exempel



Visar hur man ställer in avståndstypen för siffran.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Denna effekt stöds endast i nyare versioner av MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
