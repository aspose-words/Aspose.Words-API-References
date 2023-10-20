---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words für .NET
description: FieldOptions PreProcessCulture eigendom. Ruft die Kultur ab oder legt sie fest um Feldwerte vorzuverarbeiten in C#.
type: docs
weight: 170
url: /de/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Ruft die Kultur ab oder legt sie fest, um Feldwerte vorzuverarbeiten.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Bemerkungen

Derzeit wirkt sich diese Eigenschaft nur auf den Wert aus[`FieldDocProperty`](../../fielddocproperty/) Feld.

Der Standardwert ist`Null` . Wenn diese Eigenschaft auf festgelegt ist`Null` , Die[`FieldDocProperty`](../../fielddocproperty/)Der Wert des Feldes ist preprocessed mit der Kultur, die von gesteuert wird[`FieldUpdateCultureSource`](../fieldupdateculturesource/) Eigentum.

## Beispiele

Zeigt, wie die Vorverarbeitungskultur festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie die Kultur fest, nach der einige Felder ihre angezeigten Werte formatieren.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// Das DOCPROPERTY-Feld zeigt sein Ergebnis entsprechend der Vorverarbeitungskultur formatiert an
// wir haben auf Deutsch eingestellt. Das Feld zeigt Datum/Uhrzeit im Format „tt.mm.jjjj hh:mm“ an.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Nach dem Wechsel zur invarianten Kultur verwendet das DOCPROPERTY-Feld das Format „MM/TT/JJJJ hh:mm“.
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
