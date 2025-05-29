---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldOptions LegacyNumberFormat“, um veraltete Zahlenformate für Felder zu aktivieren oder zu deaktivieren und so die Kompatibilität und Leistung zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Ruft den Wert ab oder legt ihn fest, der angibt, ob das veraltete Zahlenformat (vor AW 13.10) für Felder aktiviert ist oder nicht.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf`WAHR`, Vorlagensymbol „#“ funktionierte wie in .net: . Ersetzt das Rautezeichen durch die entsprechende Ziffer, falls vorhanden; andernfalls erscheint kein Symbol in der Ergebniszeichenfolge.

Wenn diese Eigenschaft auf`FALSCH`, das Vorlagensymbol "#" funktioniert wie MS Word: Dieses Formatelement gibt die erforderlichen numerischen Stellen an, die im Ergebnis angezeigt werden sollen. Wenn das Ergebnis an dieser Stelle keine Ziffer enthält, zeigt MS Word ein Leerzeichen an. Beispiel: { = 9 + 6 \# $### } zeigt $ 15 an.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie die veraltete Zahlenformatierung für Felder aktiviert wird.

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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
