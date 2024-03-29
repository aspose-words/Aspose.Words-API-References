---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words für .NET
description: Font LocaleId eigendom. Ruft die Gebietsschemakennung Sprache der formatierten Zeichen ab oder legt diese fest in C#.
type: docs
weight: 200
url: /de/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Ruft die Gebietsschemakennung (Sprache) der formatierten Zeichen ab oder legt diese fest.

```csharp
public int LocaleId { get; set; }
```

## Bemerkungen

Die Liste der Gebietsschema-IDs finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Beispiele

Zeigt, wie das Gebietsschema des Texts festgelegt wird, den wir mit einem Dokumentersteller hinzufügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir das Gebietsschema der Schriftart auf Englisch setzen und russischen Text einfügen,
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
