---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die UseInvariantCultureNumberFormat-Eigenschaft von FieldOptions, um die Zahlenformatierung mit invarianter Kultur für eine konsistente Datenverarbeitung einfach zu verwalten.
type: docs
weight: 210
url: /de/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Ruft den Wert ab oder legt ihn fest, der angibt, ob das Zahlenformat mit invarianter Kultur analysiert wird oder nicht

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf`WAHR` das Zahlenformat wird aus einer invarianten Kultur übernommen.

Wenn diese Eigenschaft auf`FALSCH` , das Zahlenformat wird aus der Kultur des aktuellen Threads übernommen.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie Zahlen entsprechend der invarianten Kultur formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

    // Manchmal werden die Zahlen in bestimmten Kulturen nicht korrekt formatiert.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// Um dies zu beheben, könnten wir die Kultur für den gesamten Thread ändern.
// Eine andere Möglichkeit, dies zu beheben, besteht darin, dieses Flag zu setzen.
// wodurch alle Felder beim Formatieren von Zahlen die invariante Kultur verwenden.
// Auf diese Weise können wir vermeiden, die Kultur für den gesamten Thread zu ändern.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
