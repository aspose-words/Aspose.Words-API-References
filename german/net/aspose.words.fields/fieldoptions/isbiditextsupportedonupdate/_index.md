---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft den Wert ab oder legt ihn fest der angibt ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht.
type: docs
weight: 150
url: /de/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft auf festgelegt ist`WAHR`werden zusätzliche Schritte ausgeführt, um während der Aktualisierung ein mit der Rechts-nach-Links-Sprache (d. h. Arabisch oder Hebräisch) kompatibles Feldergebnis zu erzeugen.

Wenn diese Eigenschaft auf festgelegt ist`FALSCH` und die Rechts-nach-Links-Sprache verwendet wird, kann die Korrektheit des Felds result nach seiner Aktualisierung nicht garantiert werden.

Der Standardwert ist`FALSCH`.

### Beispiele

Zeigt, wie Sie FieldOptions verwenden, um sicherzustellen, dass die Feldaktualisierung bidirektionalen Text vollständig unterstützt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Stellen Sie sicher, dass alle Feldoperationen mit Text von rechts nach links wie erwartet ausgeführt werden.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Verwenden Sie einen Dokumentersteller, um ein Feld einzufügen, das den von rechts nach links verlaufenden Text enthält.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


