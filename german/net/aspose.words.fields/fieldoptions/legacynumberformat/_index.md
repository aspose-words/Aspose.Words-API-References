---
title: FieldOptions.LegacyNumberFormat
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft den Wert ab oder legt diesen fest der angibt ob das alte Zahlenformat früher als AW 13.10 für Felder aktiviert ist oder nicht.
type: docs
weight: 160
url: /de/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Ruft den Wert ab oder legt diesen fest, der angibt, ob das alte Zahlenformat (früher als AW 13.10) für Felder aktiviert ist oder nicht.

```csharp
public bool LegacyNumberFormat { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft auf festgelegt ist`WAHR`, Vorlagensymbol „#“ funktionierte wie in .net: Ersetzt das Nummernzeichen durch die entsprechende Ziffer, falls vorhanden; andernfalls werden in der Ergebniszeichenfolge keine Symbole angezeigt.

Wenn diese Eigenschaft auf festgelegt ist`FALSCH`, das Vorlagensymbol „#“ funktioniert wie in MS Word: Dieses Formatelement gibt die erforderlichen numerischen Stellen an, die im Ergebnis angezeigt werden sollen. Wenn das Ergebnis an dieser Stelle keine Ziffer enthält, zeigt MS Word ein Leerzeichen an. Beispiel: { = 9 + 6 \# $### } zeigt 15 $ an.

Der Standardwert ist`FALSCH`.

### Beispiele

Zeigt, wie Sie die alte Zahlenformatierung für Felder aktivieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


