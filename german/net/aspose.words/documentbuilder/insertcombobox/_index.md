---
title: DocumentBuilder.InsertComboBox
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt ein ComboboxFormularfeld an der aktuellen Position ein.
type: docs
weight: 280
url: /de/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Fügt ein Combobox-Formularfeld an der aktuellen Position ein.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name des Formularfelds. Kann eine leere Zeichenfolge sein. Der Wert, der länger als 20 Zeichen ist, wird abgeschnitten. |
| items | String[] | Die Elemente der ComboBox. Maximal 25 Artikel. |
| selectedIndex | Int32 | Der Index des ausgewählten Elements in der ComboBox. |

### Rückgabewert

Der gerade eingefügte Formularfeldknoten.

### Bemerkungen

Wenn Sie einen Namen für das Formularfeld angeben, wird automatisch ein Lesezeichen mit demselben Namen erstellt.

### Beispiele

Zeigt, wie ein Kombinationsfeld-Formularfeld in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Formular ein, das den Benutzer auffordert, eines der Elemente aus dem Menü auszuwählen.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


