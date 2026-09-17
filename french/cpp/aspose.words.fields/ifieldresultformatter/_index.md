---
title: "Aspose::Words::Fields::IFieldResultFormatter interface"
linktitle: "IFieldResultFormatter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::IFieldResultFormatter interface. Implémentez cette interface si vous souhaitez contrôler la façon dont le résultat du champ est formaté en C++."
type: docs
weight: 121000
url: /fr/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Implémentez cette interface si vous souhaitez contrôler la façon dont le résultat du champ est formaté.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Appelé lorsque Aspose.Words applique un commutateur de format de capitalisation, c.-à-d. \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Appelé lorsque Aspose.Words applique un commutateur de format numérique, c.-à-d. \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Appelé lorsque Aspose.Words applique un commutateur de format date/heure, c.-à-d. \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Appelé lorsque Aspose.Words applique un commutateur de format numérique, c.-à-d. \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
