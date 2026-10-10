---
title: "Aspose::Words::Saving::SaveOutputParameters klass"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::SaveOutputParameters-klass. Detta objekt returneras till anroparen efter att ett dokument har sparats och innehåller ytterligare information som har genererats eller beräknats under sparningsoperationen. Anroparen kan använda eller ignorera detta objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Detta objekt returneras till anroparen efter att ett dokument har sparats och innehåller ytterligare information som har genererats eller beräknats under sparningsoperationen. Anroparen kan använda eller ignorera detta objekt. För att lära dig mer, besök dokumentationsartikeln [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Returnerar Content-Type-strängen (Internet Media Type) som identifierar typen av det sparade dokumentet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man får åtkomst till utdata parametrar för ett dokuments sparningsoperation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Efter att vi har sparat ett dokument kan vi komma åt Internet Media Type (MIME-typ) för det nyss skapade utdata-dokumentet.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Denna egenskap förändras beroende på sparformatet.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
