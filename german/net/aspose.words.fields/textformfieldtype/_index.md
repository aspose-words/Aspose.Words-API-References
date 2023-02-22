---
title: Enum TextFormFieldType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.TextFormFieldType opsomming. Gibt den Typ eines Textformularfelds an.
type: docs
weight: 2590
url: /de/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Gibt den Typ eines Textformularfelds an.

```csharp
public enum TextFormFieldType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Regular | `0` | Das Textformularfeld kann beliebigen Text enthalten. |
| Number | `1` | Das Textformularfeld darf nur Zahlen enthalten. |
| Date | `2` | Das Textformularfeld kann nur einen gültigen Datumswert enthalten. |
| CurrentDate | `3` | Der Wert des Textformularfelds ist das aktuelle Datum, an dem das Feld aktualisiert wird. |
| CurrentTime | `4` | Der Wert des Textformularfelds ist die aktuelle Zeit, zu der das Feld aktualisiert wird. |
| Calculated | `5` | Der Wert des Textformularfelds wird aus dem in angegebenen Ausdruck berechnet[`TextInputDefault`](../formfield/textinputdefault/) Eigentum. |

### Beispiele

Zeigt, wie Formularfelder erstellt werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Formularfelder sind Objekte im Dokument, mit denen der Benutzer interagieren kann, indem er zur Eingabe von Werten aufgefordert wird.
// Wir können sie mit einem Document Builder erstellen, und unten sind zwei Möglichkeiten, dies zu tun.
// 1 - Einfache Texteingabe:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Kombinationsfeld mit Aufforderungstext und einer Reihe möglicher Werte:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


