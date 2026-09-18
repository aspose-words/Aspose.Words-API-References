---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interface. Stellt den Befragten für Benutzeraufforderungen während der Feldaktualisierung in C++ dar."
type: docs
weight: 125000
url: /de/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Stellt die Antwort auf Benutzeraufforderungen während der Feldaktualisierung dar.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | Wenn implementiert, gibt sie eine Antwort des Benutzers auf die Aufforderung zurück. Ihre Implementierung sollte **null** zurückgeben, um anzuzeigen, dass der Benutzer nicht auf die Eingabeaufforderung reagiert hat (d. h. der Benutzer hat die Schaltfläche Abbrechen im Eingabeaufforderungsfenster gedrückt). |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
