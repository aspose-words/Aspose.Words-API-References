---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond Methode"
linktitle: "Respond"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond Methode. Wenn implementiert, gibt sie eine Antwort des Benutzers auf die Eingabeaufforderung zurück. Ihre Implementierung sollte null zurückgeben, um anzuzeigen, dass der Benutzer nicht auf die Eingabeaufforderung reagiert hat (d. h. der Benutzer hat die Abbrechen‑Schaltfläche im Eingabefenster gedrückt) in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


Wenn implementiert, gibt sie eine Antwort des Benutzers auf die Aufforderung zurück. Ihre Implementierung sollte **null** zurückgeben, um anzuzeigen, dass der Benutzer nicht auf die Eingabeaufforderung reagiert hat (d. h. der Benutzer hat die Schaltfläche Abbrechen im Eingabeaufforderungsfenster gedrückt).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| promptText | System::String | Prompt‑Text (d. h. Titel des Eingabefensters). |
| defaultResponse | System::String | Standard‑Benutzerantwort (d. h. Anfangswert im Eingabefenster). |

### ReturnValue

Benutzerantwort (d. h. bestätigter Wert im Eingabefenster).

## Siehe auch

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
