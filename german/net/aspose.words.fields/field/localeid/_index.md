---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words für .NET
description: Field LocaleId eigendom. Ruft die LCID des Felds ab oder legt sie fest in C#.
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

Zeigt, wie man ein Feld einfügt und mit seinem Gebietsschema arbeitet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein DATE-Feld einfügen und dann das angezeigte Datum ausdrucken.
// Die aktuelle Kultur Ihres Threads bestimmt die Formatierung des Datums.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// Eine Änderung der Kultur unseres Threads wirkt sich auf das Ergebnis des DATE-Felds aus.
// Eine andere Möglichkeit, das DATE-Feld dazu zu bringen, ein Datum in einer anderen Kultur anzuzeigen, ist die Verwendung seiner LocaleId-Eigenschaft.
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
