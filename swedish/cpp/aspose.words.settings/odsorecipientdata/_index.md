---
title: "Aspose::Words::Settings::OdsoRecipientData-klass"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::OdsoRecipientData-klass. Representerar information om en enskild post i en extern datakälla som ska uteslutas från kopplad utskrift. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Representerar information om en enskild post i en extern datakälla som ska uteslutas från mail merge. För att lära dig mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Returnerar en djup klon av detta objekt. |
| [get_Active](./get_active/)() const | Anger om posten från datakällan ska importeras till ett dokument när kopplad utskrift utförs. Standardvärdet är **true**. |
| [get_Column](./get_column/)() const | Anger kolumnen i datakällan som innehåller unik data för den aktuella posten. Standardvärdet är 0. |
| [get_Hash](./get_hash/)() const | Representerar hash‑koden för denna post. Ibland använder Microsoft Word [Hash](./get_hash/) för en hel post istället för ett [UniqueTag](./get_uniquetag/)-värde. Standardvärdet är 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Anger innehållet i en given post i kolumnen som innehåller unik data. Standardvärdet är **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Anger om posten från datakällan ska importeras till ett dokument när kopplad utskrift utförs. Standardvärdet är **true**. |
| [set_Column](./set_column/)(int32_t) | Anger kolumnen i datakällan som innehåller unik data för den aktuella posten. Standardvärdet är 0. |
| [set_Hash](./set_hash/)(int32_t) | Representerar hash‑koden för denna post. Ibland använder Microsoft Word [Hash](./get_hash/) för en hel post istället för ett [UniqueTag](./get_uniquetag/)-värde. Standardvärdet är 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Anger innehållet i en given post i kolumnen som innehåller unik data. Standardvärdet är **null**. |
| static [Type](./type/)() |  |
## Anmärkningar


Om en post ska slås samman i ett sammanslaget dokument behövs ingen information om den posten. Men om en given post inte ska slås samman i ett sammanslaget dokument ska värdet för den unika nyckeln för den posten lagras i egenskapen [UniqueTag](./get_uniquetag/) för detta objekt för att indikera detta undantag.
## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
