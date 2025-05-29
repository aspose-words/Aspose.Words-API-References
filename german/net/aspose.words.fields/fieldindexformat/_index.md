---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.FieldIndexFormat für anpassbare FieldIndex-Formatierungen in Ihren Dokumenten. Verbessern Sie mühelos die Struktur Ihres Dokuments!
type: docs
weight: 2480
url: /de/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Gibt die Formatierung für die[`FieldIndex`](../fieldindex/) Felder in einem Dokument.

```csharp
public enum FieldIndexFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Template | `0` | Aus der Vorlage. |
| Classic | `1` | Klassiker. |
| Fancy | `2` | Schick. |
| Modern | `3` | Modern. |
| Bulleted | `4` | Mit Aufzählungszeichen versehen. |
| Formal | `5` | Formell. |
| Simple | `6` | Einfach. |

## Beispiele

Zeigt, wie FieldIndex-Felder formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
