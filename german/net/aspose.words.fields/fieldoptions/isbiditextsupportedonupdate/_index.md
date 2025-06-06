---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words für .NET
description: Prüfen Sie, ob die bidirektionale Textunterstützung in FieldOptions aktiviert ist. Verwalten Sie Textaktualisierungen ganz einfach für erweiterte mehrsprachige Funktionalität.
type: docs
weight: 150
url: /de/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Ruft den Wert ab oder legt ihn fest, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft auf`WAHR`werden zusätzliche Schritte ausgeführt, um während der Aktualisierung ein von rechts nach links (also mit der Sprache ) kompatibles Feldergebnis (also Arabisch oder Hebräisch) zu erzeugen.

Wenn diese Eigenschaft auf`FALSCH` und eine von rechts nach links verlaufende Sprache verwendet wird, kann die Richtigkeit des Felds result nach seiner Aktualisierung nicht garantiert werden.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie Sie mithilfe von FieldOptions sicherstellen, dass die Feldaktualisierung bidirektionalen Text vollständig unterstützt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

    // Stellen Sie sicher, dass alle Feldoperationen mit Text, der von rechts nach links geschrieben wird, wie erwartet ausgeführt werden.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Verwenden Sie einen Dokumentgenerator, um ein Feld einzufügen, das den von rechts nach links verlaufenden Text enthält.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
