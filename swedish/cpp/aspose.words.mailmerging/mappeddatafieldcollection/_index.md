---
title: "Aspose::Words::MailMerging::MappedDataFieldCollection class"
linktitle: "MappedDataFieldCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::MappedDataFieldCollection class. Tillåter automatisk mappning mellan namn på fält i din datakälla och namn på mail merge‑fält i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Tillåter att automatiskt mappa mellan namn på fält i din datakälla och namn på mail merge‑fält i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Lägger till en ny fältmappning. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [ContainsKey](./containskey/)(const System::String\&) | Bestämmer om en mappning från det angivna fältet i dokumentet finns i samlingen. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Bestämmer om en mappning från det angivna fältet i datakällan finns i samlingen. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett dictionary‑enumeratorobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Hämtar eller anger namnet på fältet i datakällan som är associerat med det angivna mail merge‑fältet. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Hämtar eller anger namnet på fältet i datakällan som är associerat med det angivna mail merge‑fältet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort en fältmappning. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Anmärkningar


Detta är implementerat som en samling av strängnycklar till strängvärden. Nycklarna är namnen på mail merge‑fält i dokumentet och värdena är namnen på fält i din datakälla.

## Se även

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
