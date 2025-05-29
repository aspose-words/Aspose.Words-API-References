---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie FieldOptions PreProcessCulture Ihre Datenverarbeitung verbessert, indem es Feldwertkulturen für mehr Genauigkeit und Effizienz anpasst.
type: docs
weight: 170
url: /de/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Ruft die Kultur zur Vorverarbeitung von Feldwerten ab oder legt sie fest.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Bemerkungen

Derzeit betrifft diese Eigenschaft nur den Wert des[`FieldDocProperty`](../../fielddocproperty/) Feld.

Der Standardwert ist`null` Wenn diese Eigenschaft auf`null` , Die[`FieldDocProperty`](../../fielddocproperty/) Der Wert des Feldes ist vorverarbeitet mit der Kultur, die durch das[`FieldUpdateCultureSource`](../fieldupdateculturesource/) Eigentum.

## Beispiele

Zeigt, wie die Vorverarbeitungskultur festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie die Kultur fest, nach der einige Felder ihre angezeigten Werte formatieren.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Das DOCPROPERTY-Feld zeigt sein Ergebnis entsprechend der Vorverarbeitungskultur formatiert an
// Wir haben es auf Deutsch eingestellt. Das Feld zeigt Datum und Uhrzeit im Format "TT.MM.JJJJ hh:MM" an.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Nach dem Wechsel zur invarianten Kultur verwendet das Feld DOCPROPERTY das Format „mm/dd/yyyy hh:mm“.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
