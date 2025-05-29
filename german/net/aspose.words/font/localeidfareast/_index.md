---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Font LocaleIdFarEast“, um Gebietsschemakennungen für formatierte asiatische Zeichen einfach zu verwalten und so Ihre mehrsprachigen Anwendungen zu verbessern.
type: docs
weight: 220
url: /de/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Ruft die Gebietsschemakennung (Sprache) der formatierten asiatischen Zeichen ab oder legt sie fest.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Bemerkungen

Die Liste der Gebietsschemakennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Beispiele

Zeigt, wie man Text in einer fernöstlichen Sprache einfügt und formatiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie die Schrifteinstellungen an, die der Dokumentgenerator auf jeden eingefügten Text anwendet.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Benennen Sie „FarEast“-Äquivalente für unsere Schriftart und unser Gebietsschema.
// Wenn der Builder asiatische Zeichen mit dieser Font-Konfiguration einfügt, dann wird jeder Lauf, der
// Diese Zeichen werden mit der Schriftart/Gebietsschema „FarEast“ anstelle der Standardeinstellung angezeigt.
// Dies kann nützlich sein, wenn eine westliche Schriftart keine ideale Darstellung für asiatische Zeichen bietet.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Dieser Text wird in der Standardschriftart/-gebietsschema angezeigt.
builder.Writeln("Hello world!");

// Da es sich um asiatische Zeichen handelt, werden bei diesem Lauf unsere Schriftart-/Gebietsschema-Äquivalente „FarEast“ angewendet.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
