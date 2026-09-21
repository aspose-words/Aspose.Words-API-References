---
title: "Aspose::Words::Saving::CssSavingArgs klass"
linktitle: "CssSavingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::CssSavingArgs klass. Tillhandahåller data för CssSaving()-händelsen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Tillhandahåller data för [CssSaving()](../icsssavingcallback/csssaving/) händelsen. För att lära dig mer, besök dokumentationsartikeln [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class CssSavingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Tillåter att ange strömmen där CSS‑informationen ska sparas. |
| [get_Document](./get_document/)() const | Hämtar dokumentobjektet som för närvarande sparas. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Tillåter att ange om CSS ska exporteras till fil och bäddas in i HTML‑dokumentet. Standard är **true**. När denna egenskap är **false** kommer CSS‑informationen inte att sparas till en CSS‑fil och inte att bäddas in i HTML‑dokumentet. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat CSS‑information. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sättare för [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Tillåter att ange om CSS ska exporteras till fil och bäddas in i HTML‑dokumentet. Standard är **true**. När denna egenskap är **false** kommer CSS‑informationen inte att sparas till en CSS‑fil och inte att bäddas in i HTML‑dokumentet. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Sättare för [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Anmärkningar


Som standard, när Aspose.Words sparar ett dokument till HTML, sparas CSS‑information inline (som ett värde för **style**‑attributet på varje element).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

För att spara CSS i en ström, använd egenskapen [CssStream](./get_cssstream/).

För att förhindra att CSS sparas i en fil och bäddas in i HTML‑dokumentet, använd egenskapen [IsExportNeeded](./get_isexportneeded/).
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
