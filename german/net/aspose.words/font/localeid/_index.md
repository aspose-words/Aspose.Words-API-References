---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „Font LocaleId“ Ihre Textformatierung verbessert, indem sie Gebietsschemakennungen für verschiedene Zeichensprachen verwaltet. Verbessern Sie noch heute Ihren Code!
type: docs
weight: 200
url: /de/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Ruft die Gebietsschemakennung (Sprache) der formatierten Zeichen ab oder legt sie fest.

```csharp
public int LocaleId { get; set; }
```

## Bemerkungen

Die Liste der Gebietsschemakennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Beispiele

Zeigt, wie das Gebietsschema des Textes festgelegt wird, den wir mit einem Dokumentgenerator hinzufügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir die Sprache der Schriftart auf Englisch einstellen und russischen Text einfügen,
// Die Rechtschreibprüfung für das englische Gebietsschema erkennt den Text nicht und erkennt ihn als Rechtschreibfehler.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Legen Sie ein passendes Gebietsschema für den Text fest, den wir hinzufügen möchten, um die entsprechende Rechtschreibprüfung anzuwenden.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
