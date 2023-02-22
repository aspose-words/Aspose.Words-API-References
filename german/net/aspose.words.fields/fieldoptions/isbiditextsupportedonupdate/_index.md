---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft den Wert ab oder legt ihn fest der angibt ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht.
type: docs
weight: 130
url: /de/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft auf eingestellt ist **Stimmt**, werden zusätzliche Schritte durchgeführt, um während seiner Aktualisierung ein rechts-nach-links-Sprache (dh Arabisch oder Hebräisch) kompatibles Feldergebnis zu erzeugen.

Wenn diese Eigenschaft auf eingestellt ist **FALSCH** und die Sprache von rechts nach links verwendet wird, kann die Korrektheit des Felds result nach seiner Aktualisierung nicht garantiert werden.

Der Standardwert ist **FALSCH**.

### Beispiele

Zeigt, wie FieldOptions verwendet wird, um sicherzustellen, dass die Feldaktualisierung vollständig bidirektionalen Text unterstützt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Stellen Sie sicher, dass alle Feldoperationen mit Text von rechts nach links wie erwartet ausgeführt werden. 
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Verwenden Sie einen Dokumentenersteller, um ein Feld einzufügen, das den von rechts nach links verlaufenden Text enthält.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


