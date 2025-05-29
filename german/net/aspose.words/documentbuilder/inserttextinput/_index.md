---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words für .NET
description: Fügen Sie mühelos Textformularfelder mit der InsertTextInput-Methode von DocumentBuilder hinzu. Verbessern Sie noch heute die Interaktivität und Benutzerfreundlichkeit Ihres Dokuments!
type: docs
weight: 510
url: /de/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Fügt an der aktuellen Position ein Textformularfeld ein.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. |
| type | TextFormFieldType | Gibt den Typ des Textformularfelds an. |
| format | String | Formatzeichenfolge, die zum Formatieren des Werts des Formularfelds verwendet wird. |
| fieldValue | String | Text, der im Feld angezeigt wird. |
| maxLength | Int32 | Maximale Länge, die der Benutzer in das Formularfeld eingeben kann. Für unbegrenzte Länge auf Null setzen. |

### Rückgabewert

Der gerade eingefügte Formularfeldknoten.

## Bemerkungen

Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

## Beispiele

Zeigt, wie ein Texteingabeformularfeld in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Formular ein, das den Benutzer zur Eingabe von Text auffordert.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Zeigt, wie ein Texteingabeformularfeld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Fügen Sie ein Texteingabefeld ein, in das der Benutzer klicken und Text eingeben kann.
// Weisen Sie einen Platzhaltertext zu, den der Benutzer überschreiben und weitergeben kann
// eine maximale Textlänge von 0, um keine Begrenzung für den Inhalt des Formularfelds anzuwenden.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Das Formularfeld wird in Form eines „Eingabe“-HTML-Tags mit dem Typ „Text“ angezeigt.
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

Zeigt, wie Formularfelder erstellt werden.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Formularfelder sind Objekte im Dokument, mit denen der Benutzer interagieren kann, indem er zur Eingabe von Werten aufgefordert wird.
// Wir können sie mit einem Dokumentgenerator erstellen. Im Folgenden finden Sie zwei Möglichkeiten dazu.
// 1 - Einfache Texteingabe:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Kombinationsfeld mit Eingabeaufforderungstext und einem Bereich möglicher Werte:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Siehe auch

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
