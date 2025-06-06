---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words für .NET
description: Verwalten Sie die LocaleId-Eigenschaft Ihres Felds mühelos. Rufen Sie die LCID ab oder legen Sie sie fest, um die Lokalisierung und Benutzerfreundlichkeit Ihrer Anwendungen zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Ruft die LCID des Felds ab oder legt sie fest.

```csharp
public int LocaleId { get; set; }
```

## Beispiele

Zeigt, wie ein Feld eingefügt und mit seinem Gebietsschema gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein DATE-Feld ein und drucken Sie dann das darin angezeigte Datum.
// Die aktuelle Kultur Ihres Threads bestimmt die Formatierung des Datums.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Das Ändern der Kultur unseres Threads wirkt sich auf das Ergebnis des DATE-Felds aus.
// Eine andere Möglichkeit, im Feld DATE ein Datum in einer anderen Kultur anzuzeigen, besteht darin, seine LocaleId-Eigenschaft zu verwenden.
// Auf diese Weise können wir vermeiden, die Kultur des Threads zu ändern, um diesen Effekt zu erzielen.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
